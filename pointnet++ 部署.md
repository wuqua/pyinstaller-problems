## [Pyinstaller打包]()

```
pyinstaller -D test_copy.py hidden-import tensorflow.contrib
```

### [问题一：]()

```
cd dist/test_copy/
sudo cp _pywrap_tensorflow_internal.so  tensorflow/python/.
sudo rm  libstdc++.so.6
sudo cp /home/think/.conda/envs/pointnet/lib/libstdc++.so.6.0.26 /home/think/siemens/tensorflow/pointnet++/dist/test_copy/.
sudo ln -s libstdc++.so.6.0.26 libstdc++.so.6
strings libstdc++.so.6 | grep CXXABI
```

### [问题二]()：

```
hiddenimports=['tensorflow.contrib','celery.*', 'celery.loaders.app', 'celery.app.amqp', 'kombu.transport.redis', 'celery.backends', 'celery.apps', 'celery.events', 'celery.worker', 'celery.bin', 'celery.concurrency', 'celery.contrib', 'celery.fixups', 'celery.security', 'celery.task', 'celery.utils', 'celery.backends.redis', 'celery.app.events','celery.fixups.django'],
```

### [问题三]()：
```

```
