## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:08ed915454c269e6e6926ef3fc6b561a218cbc733a364ed956eccd48206a6774
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

### `debian:bullseye-backports` - linux; amd64

```console
$ docker pull debian@sha256:91e6da93e3ea2624f2285009163d4da5c9bf85fb1d15e18b693f8b8e385ae054
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55099415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:543d38697ee8da8482cfc82e868cdc3b1ea1c965a21ef1e02725ecb6b1aaec5e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:05 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 13 Jun 2024 01:21:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:21:10 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae9dbdeca981eb6513f5812e966c7f90fd17180da8d0190d27934ba32985290`  
		Last Modified: Thu, 13 Jun 2024 01:26:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:77568a0abe7227c0dc0a13448f7e208ffd9a5870056656c8de1add8bb7f18d91
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52603259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ce5be3c5f94abc27ecacfb5db8148fb116bf9eca5c3ae6876c4e3dd26e3435`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:40 GMT
ADD file:e9d8f0f7fb10978e8599b4d65173747a249b36470beb002a75b03faf3b15e953 in / 
# Thu, 13 Jun 2024 00:48:41 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:48:43 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:257495c53b4c673d8b6401bad898f12d6b9f0119d3414c2dbb1f82162a4269c8`  
		Last Modified: Thu, 13 Jun 2024 00:51:58 GMT  
		Size: 52.6 MB (52603036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37c81b8d17b5c4b7eea999c2c173576cf77c1e00c75782e3144fd80bb0f28cb1`  
		Last Modified: Thu, 13 Jun 2024 00:52:10 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:19bbf512149339813a598c62dd5912ee96742cb9453afc3570e28bc62a0a86cb
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50256654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0522d26c699e2ebd4d1d1b0b7f02b0dcfadf84b526e5f8edcaaa3b7fc2dc93b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:50 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Thu, 13 Jun 2024 00:57:51 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:57:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c064313f9413dadd8cc7297f37107ee093b2a20d9535c1fc44450c34e42fd4c`  
		Last Modified: Thu, 13 Jun 2024 01:02:11 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6165ec2b65f228898b614d5ad4558b5cb2c7eae319f33cd1aa62bde4186b6ee1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53739804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbdd5cc749a30baa83caf2fb9560d414b04c170ee859ed637d27abf80db1c197`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:40:00 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efee6a41b4e50ac6e5994b0cc4f647147b9d4502d9bec94941b274ffe3c9b266`  
		Last Modified: Thu, 13 Jun 2024 00:43:43 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:1b3688e9ac2b182e50f9536950896e003836967927cccdfd9d55a305a6b7d6ab
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56076764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:247c7d3f641bd69078552745bad69c355e96d0ffcc756d8c7bc9aa05d52d128c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:07 GMT
ADD file:fc81ef6f19f37bfa7f991304cb9f2ad236462384e498e18c844726149b1fbf03 in / 
# Thu, 13 Jun 2024 00:39:07 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:39:11 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:ab8c2df85dcd39d367cf1116e6aa73c53bbbd9e40b1c09e65b70b58871ceff91`  
		Last Modified: Thu, 13 Jun 2024 00:43:45 GMT  
		Size: 56.1 MB (56076538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c6daaa1898ff53cc229f7873601ac380d8f328c589729e8e1cba07cb53d393`  
		Last Modified: Thu, 13 Jun 2024 00:43:57 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:cfa8be9c5080706b5cb78aa8da9063b97050b7dbcee357c7ded73ae803a9aea5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53322730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cbf058adbd36dd5bc7f53db2051538969c3498066693b4b7965b352737b80cc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:11:08 GMT
ADD file:2fd9c13efc7b13ca68928f53acc0c79d5841bd49e5aea46b2e1906120bba2a4f in / 
# Thu, 13 Jun 2024 01:11:14 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:11:29 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6c9f7b7d6baf92c8cec25b325ea14db33b8c298218a5bcd368bb24184c5645b6`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 53.3 MB (53322503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5f945d1cdc70b3b504a30d262b4521614a83da89b69d4f2ad1cc62d27c0934`  
		Last Modified: Thu, 13 Jun 2024 01:22:53 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:3bc76d2e29dd1ac0745b0c31d49982a1bff48fa38ecf55fdbbc2c88e7a57f558
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (58969182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e501833f2cb771d9b62e143bc81f075a3efb7d45a50f96152607a5255e151378`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:16 GMT
ADD file:32733696002797fb377d3d8094c21c0f41f25da6f371eb4a8ecb6fa5c3ef1048 in / 
# Thu, 13 Jun 2024 01:17:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:17:24 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7afd12f588c414c122b8d3022d60effda2738a394347f5b3cbdebfe1420a8bf8`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 59.0 MB (58968957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16248f27d363a61fb2c1ec71e0545c8a9c7b312fb9c9fd3972d1bff0befca86d`  
		Last Modified: Thu, 13 Jun 2024 01:22:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:61ecc41e9db340cb4928570650189264e90c2f3cd75e39de7da7d477e2b206b8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53337765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76c97e21d9b0648fbed252db95f5bc7173bb22caa6d85f911d977055d405c37`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:42:50 GMT
ADD file:1f0333c084fe60bf682ad64dd7db93b2ca069c7e1d09bf26e7e65dedbd65b0f3 in / 
# Thu, 13 Jun 2024 00:42:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 00:43:05 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:db300ed0c60856815a390ef84dc7c5441283ec11483c9da25ac0daf34bac6e83`  
		Last Modified: Thu, 13 Jun 2024 00:47:59 GMT  
		Size: 53.3 MB (53337540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab702365fb8c3d6d2f4a86d4008df41bda8ba992b8c5fa48662269ece2c06dd`  
		Last Modified: Thu, 13 Jun 2024 00:48:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
