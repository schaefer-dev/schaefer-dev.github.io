---
layout: default
title: "Daniel Schäfer | Photography"
description: "Landscape and wildlife photography portfolio by Daniel Schäfer"
show_copyright: true
---

# Photography

A sneek peek into my photography. All images shot on Sony. All photographs show wild animals in their natural habitats, never in captivity, zoos, or staged settings.

Images load in 4k resolution on-click. Loading of the high quality version may take a second or two depending on your connection.

<script>
// ===== CONFIGURATION =====
var ENABLE_ZOOM = true;  // Set to true to enable click-to-zoom functionality
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
  { id: '20250727-A1_07949_rvnamh', caption: 'Robin in Saarbrücken, Germany 2025' },
  { id: '20251101-A1_07621_w4tp0l', caption: 'Marsh Tit in Saarbrücken, Germany 2025' },
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

// Combined gallery for navigation
var allPhotos = [];
var currentPhotoIndex = 0;

function generateGallery(photos, containerId, startIndex) {
  var html = '';
  photos.forEach(function(photo, index) {
    var globalIndex = startIndex + index;
    var thumbSize = photo.sizeParam === 'h' ? 'h_800' : 'w_800';
    var fullSize = photo.sizeParam === 'h' ? 'h_3840' : 'w_3840';
    var thumbUrl = 'https://res.cloudinary.com/dhateve93/image/upload/' + thumbSize + ',q_85,f_auto,fl_progressive/' + photo.id;
    var fullUrl = 'https://res.cloudinary.com/dhateve93/image/upload/' + fullSize + ',q_90,f_auto,fl_progressive/' + photo.id;

    // Store in global array for navigation
    allPhotos[globalIndex] = {
      fullUrl: fullUrl,
      thumbUrl: thumbUrl,
      caption: photo.caption
    };

    html += '<div class="photo-item" onclick="openLightboxByIndex(' + globalIndex + ')">';
    html += '  <img src="' + thumbUrl + '"';
    html += '       alt="' + photo.caption + '"';
    html += '       loading="lazy">';
    html += '  <div class="photo-caption">' + photo.caption + '</div>';
    html += '</div>';
  });
  document.getElementById(containerId).innerHTML = html;
}

// Generate galleries when page loads
document.addEventListener('DOMContentLoaded', function() {
  generateGallery(wildlifePhotos, 'wildlife-gallery', 0);
  generateGallery(landscapePhotos, 'landscape-gallery', wildlifePhotos.length);
});
</script>

## Wildlife Photography

<div id="wildlife-gallery" class="photo-gallery"></div>

## Landscape Photography

<div id="landscape-gallery" class="photo-gallery"></div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-close">&times;</span>
  <a id="lightbox-download" class="lightbox-download" download onclick="event.stopPropagation()">
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"></path>
      <polyline points="7 10 12 15 17 10"></polyline>
      <line x1="12" y1="15" x2="12" y2="3"></line>
    </svg>
  </a>
  <button id="lightbox-prev" class="lightbox-nav lightbox-prev" onclick="navigatePrev(event)" aria-label="Previous image">
    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <polyline points="15 18 9 12 15 6"></polyline>
    </svg>
  </button>
  <button id="lightbox-next" class="lightbox-nav lightbox-next" onclick="navigateNext(event)" aria-label="Next image">
    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
      <polyline points="9 18 15 12 9 6"></polyline>
    </svg>
  </button>
  <img id="lightbox-img" class="lightbox-content" src="" alt="">
  <div id="lightbox-caption" class="lightbox-caption"></div>
  <div id="loading-bar" class="loading-bar">
    <div id="loading-progress" class="loading-progress"></div>
    <div id="loading-text" class="loading-text">Loading high resolution...</div>
  </div>
</div>

<script>
var zoomLevel = 1;
var isPanning = false;
var startX, startY;
var translateX = 0, translateY = 0;
var progressInterval = null;
var currentProgress = 0;

function openLightboxByIndex(index) {
  currentPhotoIndex = index;
  var photo = allPhotos[index];
  openLightbox(photo.fullUrl, photo.thumbUrl, photo.caption);
  updateNavigationButtons();
}

function navigatePrev(e) {
  if (e) {
    e.stopPropagation();
    e.preventDefault();
  }
  if (currentPhotoIndex > 0) {
    openLightboxByIndex(currentPhotoIndex - 1);
  }
}

function navigateNext(e) {
  if (e) {
    e.stopPropagation();
    e.preventDefault();
  }
  if (currentPhotoIndex < allPhotos.length - 1) {
    openLightboxByIndex(currentPhotoIndex + 1);
  }
}

function updateNavigationButtons() {
  var prevBtn = document.getElementById('lightbox-prev');
  var nextBtn = document.getElementById('lightbox-next');

  // Hide/show buttons based on position
  if (currentPhotoIndex === 0) {
    prevBtn.style.opacity = '0';
    prevBtn.style.pointerEvents = 'none';
  } else {
    prevBtn.style.opacity = '';
    prevBtn.style.pointerEvents = '';
  }

  if (currentPhotoIndex === allPhotos.length - 1) {
    nextBtn.style.opacity = '0';
    nextBtn.style.pointerEvents = 'none';
  } else {
    nextBtn.style.opacity = '';
    nextBtn.style.pointerEvents = '';
  }
}

function openLightbox(fullUrl, thumbUrl, caption) {
  if (event) event.stopPropagation();

  var lightboxImg = document.getElementById('lightbox-img');
  var lightbox = document.getElementById('lightbox');
  var downloadBtn = document.getElementById('lightbox-download');
  var loadingBar = document.getElementById('loading-bar');
  var loadingProgress = document.getElementById('loading-progress');
  var loadingText = document.getElementById('loading-text');

  // Reset zoom and position
  resetZoom();

  // Show lightbox immediately with cached thumbnail (optionally blurred)
  lightbox.classList.add('active');
  document.getElementById('lightbox-caption').textContent = caption;
  document.body.style.overflow = 'hidden';

  // Set download button href to full resolution image
  downloadBtn.href = fullUrl;
  downloadBtn.download = caption.replace(/[^a-z0-9]/gi, '_') + '.jpg';

  // Set cached 800px thumbnail with blur effect
  lightboxImg.src = thumbUrl;
  lightboxImg.style.opacity = '1';
  // lightboxImg.style.filter = 'blur(5px)';
  lightboxImg.style.transform = 'scale(0.90)'; // Scale up slightly to hide blur edges

  // Show and reset loading bar
  loadingBar.style.opacity = '1';
  loadingProgress.style.width = '0%';
  loadingText.style.opacity = '1';
  currentProgress = 0;

  // Clear any existing progress interval
  if (progressInterval) {
    clearInterval(progressInterval);
  }

  // Simulated smooth progress animation (0-90% over ~5 seconds)
  // This provides immediate visual feedback while the real download happens
  var simulatedProgress = 0;
  var realProgressReceived = false;

  progressInterval = setInterval(function() {
    if (!realProgressReceived && simulatedProgress < 90) {
      // Slow down as we approach 90% to make it feel more natural
      var increment = (90 - simulatedProgress) * 0.05;
      simulatedProgress += Math.max(increment, 0.3);
      currentProgress = Math.min(simulatedProgress, 90);
      loadingProgress.style.width = currentProgress + '%';
    }
  }, 50);

  // Load the high-quality image with progress tracking
  var xhr = new XMLHttpRequest();
  xhr.open('GET', fullUrl, true);
  xhr.responseType = 'blob';

  xhr.onprogress = function(e) {
    if (e.lengthComputable) {
      var percentComplete = (e.loaded / e.total) * 100;
      realProgressReceived = true;
      // Use the real progress, but ensure it's at least as much as simulated
      currentProgress = Math.max(currentProgress, percentComplete);
      loadingProgress.style.width = currentProgress + '%';
    }
  };

  xhr.onload = function() {
    if (progressInterval) {
      clearInterval(progressInterval);
      progressInterval = null;
    }

    if (xhr.status === 200) {
      // Jump to 100% immediately
      loadingProgress.style.width = '100%';

      var blob = xhr.response;
      var objectUrl = URL.createObjectURL(blob);

      // Smoothly transition to high-quality image
      lightboxImg.style.transition = 'filter 0.5s ease, transform 0.5s ease';
      lightboxImg.src = objectUrl;
      lightboxImg.style.filter = 'blur(0)';
      lightboxImg.style.transform = 'translate(' + translateX + 'px, ' + translateY + 'px) scale(' + zoomLevel + ')';

      // Hide loading bar and text with fade out
      setTimeout(function() {
        loadingBar.style.opacity = '0';
        loadingText.style.opacity = '0';
      }, 400);

      // Remove transition after animation completes to prevent floaty panning
      setTimeout(function() {
        lightboxImg.style.transition = '';
      }, 500);

      // Clean up object URL when lightbox is closed
      lightboxImg.addEventListener('load', function() {
        setTimeout(function() {
          if (lightboxImg.src === objectUrl) {
            URL.revokeObjectURL(objectUrl);
          }
        }, 1000);
      }, { once: true });
    }
  };

  xhr.onerror = function() {
    if (progressInterval) {
      clearInterval(progressInterval);
      progressInterval = null;
    }

    // Fallback to simple image loading on error
    var highResImg = new Image();
    highResImg.onload = function() {
      lightboxImg.style.transition = 'filter 0.5s ease, transform 0.5s ease';
      lightboxImg.src = fullUrl;
      lightboxImg.style.filter = 'blur(0)';
      lightboxImg.style.transform = 'translate(' + translateX + 'px, ' + translateY + 'px) scale(' + zoomLevel + ')';

      loadingBar.style.opacity = '0';
      loadingText.style.opacity = '0';

      setTimeout(function() {
        lightboxImg.style.transition = '';
      }, 500);
    };
    highResImg.src = fullUrl;
  };

  xhr.send();
}

function closeLightbox() {
  // Clean up progress interval
  if (progressInterval) {
    clearInterval(progressInterval);
    progressInterval = null;
  }

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

  // Pan when zoomed (mouse events)
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

  // Pan when zoomed (touch events for mobile)
  document.getElementById('lightbox-img').addEventListener('touchstart', function(e) {
    if (zoomLevel > 1 && e.touches.length === 1) {
      e.preventDefault();
      e.stopPropagation();
      isPanning = true;
      startX = e.touches[0].clientX - translateX;
      startY = e.touches[0].clientY - translateY;
    }
  });

  document.getElementById('lightbox-img').addEventListener('touchmove', function(e) {
    if (isPanning && e.touches.length === 1) {
      e.preventDefault();
      translateX = e.touches[0].clientX - startX;
      translateY = e.touches[0].clientY - startY;
      updateTransform();
    }
  });

  document.getElementById('lightbox-img').addEventListener('touchend', function() {
    isPanning = false;
  });

  document.getElementById('lightbox-img').addEventListener('touchcancel', function() {
    isPanning = false;
  });
}

// Keyboard shortcuts
document.addEventListener('keydown', function(event) {
  var lightbox = document.getElementById('lightbox');

  // Only handle keyboard shortcuts when lightbox is open
  if (!lightbox.classList.contains('active')) {
    return;
  }

  if (event.key === 'Escape') {
    closeLightbox();
  } else if (event.key === 'ArrowLeft') {
    event.preventDefault();
    navigatePrev();
  } else if (event.key === 'ArrowRight') {
    event.preventDefault();
    navigateNext();
  }
});
</script>
