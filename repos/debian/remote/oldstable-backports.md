## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:8df9a160d63840fcc47fb44f42e0118047d7a71bad0a64dc945834eee0fbe192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:211fcff4a2f6ae12ae70ad9c81cd7380a2a93ca94af6130cef42f0ab0730d58c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55081625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8eb252bee4dfa8e2711fad0095fad64b28fd3421598641e2bae562e1a0f7db`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:34 GMT
ADD file:38e0ab105db32d90421178fd176f2adfe7ea5d104ab21dee8427b1857212618f in / 
# Tue, 02 Jul 2024 01:25:35 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:25:39 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9d70182e582870b85b1604eedb36c0c5540a5a9cf95a1684d0a97617fa1ce283`  
		Last Modified: Tue, 02 Jul 2024 01:29:45 GMT  
		Size: 55.1 MB (55081400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f66e1bc1ccd7f0ec794c568aa3ed16b5fee4a769840b4ba7b934eea1627a8f0`  
		Last Modified: Tue, 02 Jul 2024 01:29:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:c3dbb5275d7338c5fa01a07552e8b7946be3d4eb993975c3bfb55c076d1a87aa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52589208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0593ab321818b2646ecf0cbd67a458ee82529012b2c5ab550e40ebb7e23a3568`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:57:37 GMT
ADD file:ee32dff7181ea89337ad2e02d7ecb4ec5f28d345c74f78071c4e3919f6b995b2 in / 
# Mon, 22 Jul 2024 23:57:38 GMT
CMD ["bash"]
# Mon, 22 Jul 2024 23:57:41 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f3d4c51394c96f881a95a27d296a833b56f29bfe21e9dde8c456a2ddb371f5fe`  
		Last Modified: Tue, 23 Jul 2024 00:02:25 GMT  
		Size: 52.6 MB (52588984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29258cea2b6893d27515c7f06bb5059a28d65b366fb8e34a04e121d4dc2f4fa3`  
		Last Modified: Tue, 23 Jul 2024 00:02:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:435476e0083edafaa74b2723884b156028a329fbf79b2c9a00759cd39d053097
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50242597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061f0035f081f22aa05b03c11d2133dc6b840c89562e23e08eef1cefb97302d8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:42 GMT
ADD file:f7c4268719cac328762fc60ce7ca9b64823325c376eb6117bfbf0da28b5c966e in / 
# Tue, 23 Jul 2024 03:03:43 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:03:45 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1e558ad41278fbed583a7b21a9fd318ef6d28e3eacf34645045843f3c937eb5f`  
		Last Modified: Tue, 23 Jul 2024 03:07:52 GMT  
		Size: 50.2 MB (50242372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d67d54d36805a83eb0d49fba2cc21a62425731dc65eb7678c7130f59cfdae9`  
		Last Modified: Tue, 23 Jul 2024 03:08:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:d470c7834ce4e796d708fcabe7c41d7a92a4d06d2968afbd1376fe4fee437548
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53721887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92274a264c37afd1a658edd0a3e5116f468558097978aebdad8e9495ffbc1648`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:58 GMT
ADD file:15a04866a1a28523798f9f7254b7bfc591fd26b891018866c2f2a98fc9626132 in / 
# Tue, 02 Jul 2024 00:39:59 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 00:40:02 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8d13c62a49a498ddc0ea037d935b1e0af1c721c91f5e1cd7fc5e131c81150536`  
		Last Modified: Tue, 02 Jul 2024 00:43:21 GMT  
		Size: 53.7 MB (53721662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86eab011a00c513c96b36e05e49dfcd3df1efb0eaa9bd3c9539e7e9ce56ed3a`  
		Last Modified: Tue, 02 Jul 2024 00:43:30 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:f7a5e630ba372ea03af7d77eebd34fc88f5a1b24870cccf18207b6d18ece91d6
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56074362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469abaea97a972ec3b23b8cdf652db641cb125100ceb98999402849c9ebb7549`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:54:46 GMT
ADD file:a2e4d933154bb7355658d3c1243011705d869ab50677386bcd79b5f0c320f445 in / 
# Tue, 23 Jul 2024 03:54:46 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:54:50 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c5286ac860b08ecfbb3408d876aae1751e8c6f8c14aba43ff6a85947c0674019`  
		Last Modified: Tue, 23 Jul 2024 03:58:54 GMT  
		Size: 56.1 MB (56074137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0653645942a69871c924df1256a06f0ec621bce2eb4fc89fc1b5c93a44c413`  
		Last Modified: Tue, 23 Jul 2024 03:59:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:3ca5dcbbf47a1320c5478682638c01f4479aca380e6c514c3c389c6d4a2e2cb0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53310816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9148414659118330e56a3cb85a24980d37d4f0338ac9372441af52ffbf577018`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:39:46 GMT
ADD file:e956d8bcad7c8fb5c8e1e95af2724508b1e9a56b47874389710e5552e3742416 in / 
# Tue, 23 Jul 2024 00:39:51 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 00:40:06 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6170bbb61762f0aed25761b66e738a58b941c2da14b91747710eaca53be019ca`  
		Last Modified: Tue, 23 Jul 2024 00:51:17 GMT  
		Size: 53.3 MB (53310590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa822d1aacf9fb8b8aefd4e2a23dd1f515752456b07a5d87a2b1e61f9e69185`  
		Last Modified: Tue, 23 Jul 2024 00:51:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:d07a8aab11def6489052581f2c94d9499964a63c65f87609515e40c45a82b785
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58954906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1c5bf72c17f9978071690557220c8c9d882d0452f8c91b3170d1215f3307956`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:35 GMT
ADD file:cf8a77d9ef6ee27c54ad24ff4dc8300ec071d6e9cb41d58c8b2d0e6c215213ce in / 
# Tue, 23 Jul 2024 01:27:38 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:27:43 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:3ef7c55e110658f296887488c95f8341e0d6a334636e6b0fe8724d5a084a4663`  
		Last Modified: Tue, 23 Jul 2024 01:32:13 GMT  
		Size: 59.0 MB (58954682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e685c031a5fe5adc94c9b14405d706f504f523ede244ccc78db3ed1a9b016bb`  
		Last Modified: Tue, 23 Jul 2024 01:32:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:85f1ed905359fc5e990dfc6fa54e3bce777256705e04e4914311f1f0cf8f6ec9
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53324326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139ecc0d27f2d0e4ed07bb6c9065be195d172e906b1a183601fc9da0061a10b9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:28:40 GMT
ADD file:289754ba8557dc34825b3e6742d5236121ec135403950d6b3e3f9256a13c4af9 in / 
# Tue, 23 Jul 2024 02:28:43 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:28:51 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8868a5028b5d8a41eafe48e6da7d212ffafd43ee0483beb1e21b95d2068c0f79`  
		Last Modified: Tue, 23 Jul 2024 02:33:26 GMT  
		Size: 53.3 MB (53324103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2643657fc98c6902e34792f9d42b221205e1d712f177c58e4d01632f7d0fb3`  
		Last Modified: Tue, 23 Jul 2024 02:33:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
