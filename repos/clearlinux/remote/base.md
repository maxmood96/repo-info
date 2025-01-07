## `clearlinux:base`

```console
$ docker pull clearlinux@sha256:fb81bd95ca7407cfa9ababc20508917fd16c76731485ba0546eac19527f7f334
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clearlinux:base` - linux; amd64

```console
$ docker pull clearlinux@sha256:b6f49ce6730d8367da1170aadfe944b904df8e5295435804c1e42e021a8057be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72063293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aab9db6ef6c3b25b4def1d512d2fe3deff797e5719e99a67cf2919b9e31dfbef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 18 Dec 2024 22:33:08 GMT
MAINTAINER William Douglas <william.douglas@intel.com>
# Wed, 18 Dec 2024 22:33:08 GMT
ADD base.tar.xz / # buildkit
# Wed, 18 Dec 2024 22:33:08 GMT
RUN cd /etc &&     grep root /usr/share/defaults/etc/passwd > /etc/passwd &&     grep root /usr/share/defaults/etc/group > /etc/group &&     echo 'root:!:::::::' > /etc/shadow # buildkit
# Wed, 18 Dec 2024 22:33:08 GMT
CMD ["/bin/bash"]
```

-	Layers:
	-	`sha256:64d12590492893d5e2f130a23f68e8a7b68c7e461853b473e00038894c4b4fc8`  
		Last Modified: Tue, 24 Dec 2024 21:32:28 GMT  
		Size: 72.1 MB (72063079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b868939f5b0c0efaa45714babdd4c66ccfe0b0717ee91595d8e706c8f363eeba`  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clearlinux:base` - unknown; unknown

```console
$ docker pull clearlinux@sha256:596b9d5bd7a1a03e68b343d2a80553d9f0dfe97bd26ccca167daf34e16c8bce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 KB (6275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d539bf4afc7c5393a7089fcc8f2cbfb4c820f9f894db3be89262abcc24683e`

```dockerfile
```

-	Layers:
	-	`sha256:c2b51f7806467715245f71ab6e1a5bf39d70685b75e64a366a64d23eec65088a`  
		Last Modified: Tue, 24 Dec 2024 21:32:26 GMT  
		Size: 6.3 KB (6275 bytes)  
		MIME: application/vnd.in-toto+json
