### scikit-image
---
https://github.com/scikit-image/scikit-image

https://scikit-image.org/

```py
// skimage/io/tests/test_multi_image.py

@fixture
def imps():
  use_plugin('pil')
  paths = [os.path.join(data_dir, 'multipage_rgb.tif'),
      os.path.join(data_dir, 'no_time_for_that_tiny.gif')]
  imgs = [MultiImage(paths[0]),
    MultiImage(paths[0], conserve_memory=False),
    MultiImage(paths[1]),
    MultiImage(paths[1], conserve_memory=False),
    ImageCollection(paths[0]),
    ImageCollection(paths[1], conserve_memory=False),
    ImageCollection(os.pathsep.join(paths))]
  yeild imgs
 
  reset_plugins()

def test_shapes(imgs):
  img = imgs[-1]
  imgs = img[:]
  assert imgs[0].shape == imag[1].shape
  assert imgs[0].shape == (10, 10, 3)
```

```
```

```
```


