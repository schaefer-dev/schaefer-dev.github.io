---
layout: default
title: "Daniel Schäfer | Photography"
description: "Landscape and wildlife photography portfolio by Daniel Schäfer"
---

# Photography

A sneak peek into my photography. All images shot on Sony. All photographs show wild animals in their natural habitats, never in captivity, zoos, or staged settings.

<script>
// ===== CONFIGURATION =====
var ENABLE_ZOOM = false;  // Set to true to enable click-to-zoom functionality
// =========================

// Photo data - just add ID and caption once!
var wildlifePhotos = [
  { id: '20250613-A1_08790-Enhanced-NR-2_xc1srs', caption: 'Puffin on Runde Island, Norway 2025' },
  { id: '20250613-A1_02369-2_ig7tmg', caption: 'Puffin on Runde Island, Norway 2025' },
  { id: '20250613-A1_01332_yfolsv', caption: 'Puffin on Runde Island, Norway 2025' },
  { id: '20250613-A1_08464_iz4otn', caption: 'Puffin on Runde Island, Norway 2025' },
  { id: '20250902-A1_04583-2_z4m8sa', caption: 'Little Owl in Saarbruecken, Germany 2025' },
  { id: '20250930-A1_04174_f6pcbd', caption: 'Kingfisher in Dillingen, Germany 2025' },
  { id: '20250930-A1_00439_qhqxur', caption: 'Kingfisher in Dillingen, Germany 2025' },
  { id: '20250920-A1_05933_xsixu5', caption: 'Kingfisher in Haff Réimech, Luxembourg 2025' },
  { id: '20250727-A1_07949_rvnamh', caption: 'Rotkehlchen in Saarbrücken, Germany 2025' },
  { id: '20251101-A1_07621_w4tp0l', caption: 'Meise in Saarbrücken, Germany 2025' },
  { id: '20251021-A1_09393_popwqq', caption: 'Beared Vulture in Krumltal, Austria 2025', sizeParam: 'h' }
];

var landscapePhotos = [
  { id: '20240921-DSC09138_cafeli', caption: 'Mulagljufur Canyon, Iceland 2024' },
  { id: '20240923-DSC09864_c2spbt', caption: 'Landmannalaugar, Iceland 2024' },
  { id: '20240923-DSC00034_iakmbe', caption: 'Landmannalaugar, Iceland 2024' },
  { id: '20240925-DSC00638-Enhanced-NR_ywap2n', caption: 'Northern Lights, Iceland 2024' },
  { id: '20240925-DSC00606_kfijjl', caption: 'Northern Lights, Iceland 2024' },
  { id: '20240806-DSC02785-Enhanced-NR_hhwowj', caption: 'Milky Way at Peterberg, Germany 2024', sizeParam: 'h' },
  { id: '20240816-DSC03915_yh5ece', caption: 'Pilatus, Switzerland 2024' },
  { id: '20250612-A1_07027-HDR-Pano-Edit-2_ssghqf', caption: 'Eidsvatnet, Norway 2025' },
  { id: '20251022-A1_01072-HDR-Pano_drini7', caption: 'Heiligenblut, Austria 2025' },
  { id: '20251024-A1_01286-Pano_lg7tox', caption: 'Lake Jasna, Slovenia 2025' },
  { id: '20251024-A1_01326-HDR-Pano_tsp4hj', caption: 'Lake Jasna, Slovenia 2025' },
  { id: '20251024-A1_01541-HDR_l2bggd', caption: 'Kranjska Gora, Slovenia 2025' },
  { id: '20251025-A1_02001-HDR-Pano_gq8gsm', caption: 'Lake Bled, Slovenia 2025' },
  { id: '20251026-A1_02326_wm95wa', caption: 'Bohinjsko Jezero, Slovenia 2025' },
  { id: '20251028-A1_03784_vodphl', caption: 'Soca Valley, Slovenia 2025', sizeParam: 'h' },
  { id: '20251024-A1_01793-Pano_swwlcp', caption: 'Vršič Pass, Slovenia 2025' },
  { id: '20251029-A1_05138_etnopq', caption: 'Postojna Cave, Slovenia 2025' }

];

function generateGallery(photos, containerId) {
  var html = '';
  photos.forEach(function(photo) {
    var thumbSize = photo.sizeParam === 'h' ? 'h_800' : 'w_800';
    var fullSize = photo.sizeParam === 'h' ? 'h_3840' : 'w_3840';

    html += '<div class="photo-item" onclick="openLightbox(\'https://res.cloudinary.com/dhateve93/image/upload/' + fullSize + ',q_90,f_auto,fl_progressive/' + photo.id + '\', \'' + photo.caption + '\')">';
    html += '  <img src="https://res.cloudinary.com/dhateve93/image/upload/' + thumbSize + ',q_85,f_auto,fl_progressive/' + photo.id + '"';
    html += '       alt="' + photo.caption + '"';
    html += '       loading="lazy">';
    html += '  <div class="photo-caption">' + photo.caption + '</div>';
    html += '</div>';
  });
  document.getElementById(containerId).innerHTML = html;
}

// Generate galleries when page loads
document.addEventListener('DOMContentLoaded', function() {
  generateGallery(wildlifePhotos, 'wildlife-gallery');
  generateGallery(landscapePhotos, 'landscape-gallery');
});
</script>

## Wildlife Photography

<div id="wildlife-gallery" class="photo-gallery"></div>

## Landscape Photography

<div id="landscape-gallery" class="photo-gallery"></div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <img id="lightbox-img" class="lightbox-content" src="" alt="">
  <div id="lightbox-caption" class="lightbox-caption"></div>
</div>

<script>
var zoomLevel = 1;
var isPanning = false;
var startX, startY;
var translateX = 0, translateY = 0;

function openLightbox(imageUrl, caption) {
  event.stopPropagation();

  var lightboxImg = document.getElementById('lightbox-img');
  var lightbox = document.getElementById('lightbox');

  // Reset zoom and position
  resetZoom();

  // Always clear the old image first to prevent showing wrong image
  lightboxImg.src = '';

  // Small delay to ensure browser clears the old image
  setTimeout(function() {
    // Show lightbox
    lightbox.classList.add('active');
    document.getElementById('lightbox-caption').textContent = caption;
    document.body.style.overflow = 'hidden';

    // Set new image to allow progressive rendering
    lightboxImg.src = imageUrl;
    lightboxImg.style.opacity = '1';
  }, 10);
}

function closeLightbox() {
  document.getElementById('lightbox').classList.remove('active');
  document.body.style.overflow = 'auto';
  resetZoom();
}

function resetZoom() {
  zoomLevel = 1;
  translateX = 0;
  translateY = 0;
  updateTransform();
  updateCursor();
}

function updateTransform() {
  var lightboxImg = document.getElementById('lightbox-img');
  lightboxImg.style.transform = 'translate(' + translateX + 'px, ' + translateY + 'px) scale(' + zoomLevel + ')';
}

function updateCursor() {
  var lightboxImg = document.getElementById('lightbox-img');
  if (!ENABLE_ZOOM) {
    lightboxImg.style.cursor = 'default';
  } else if (zoomLevel > 1) {
    lightboxImg.style.cursor = 'zoom-out';
  } else {
    lightboxImg.style.cursor = 'zoom-in';
  }
}

// Zoom and pan functionality (only if enabled)
if (ENABLE_ZOOM) {
  // Mouse wheel zoom
  document.getElementById('lightbox-img').addEventListener('wheel', function(e) {
    e.preventDefault();
    e.stopPropagation();

    var delta = e.deltaY > 0 ? -0.2 : 0.2;
    zoomLevel = Math.min(Math.max(1, zoomLevel + delta), 2); // Limit zoom between 1x and 2x

    if (zoomLevel === 1) {
      translateX = 0;
      translateY = 0;
    }

    updateTransform();
    updateCursor();
  });

  // Click to toggle zoom (simple toggle between 1x and 2x)
  document.getElementById('lightbox-img').addEventListener('click', function(e) {
    e.stopPropagation();

    if (zoomLevel > 1) {
      resetZoom();
    } else {
      zoomLevel = 2;
      updateTransform();
      updateCursor();
    }
  });

  // Right-click to reset zoom
  document.getElementById('lightbox-img').addEventListener('contextmenu', function(e) {
    e.preventDefault();
    e.stopPropagation();
    resetZoom();
  });

  // Pan when zoomed
  document.getElementById('lightbox-img').addEventListener('mousedown', function(e) {
    if (zoomLevel > 1) {
      e.preventDefault();
      e.stopPropagation();
      isPanning = true;
      startX = e.clientX - translateX;
      startY = e.clientY - translateY;
    }
  });

  document.addEventListener('mousemove', function(e) {
    if (isPanning) {
      e.preventDefault();
      translateX = e.clientX - startX;
      translateY = e.clientY - startY;
      updateTransform();
    }
  });

  document.addEventListener('mouseup', function() {
    isPanning = false;
  });
}

// Close lightbox on Escape key
document.addEventListener('keydown', function(event) {
  if (event.key === 'Escape') {
    closeLightbox();
  }
});
</script>
