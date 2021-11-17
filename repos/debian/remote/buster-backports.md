## `debian:buster-backports`

```console
$ docker pull debian@sha256:f04c4cfcc192382273af1c1423ebba9d5b436face7e47b5ff5b1497529e56e1e
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

### `debian:buster-backports` - linux; amd64

```console
$ docker pull debian@sha256:fa16640823e33a5c94dab6bcb16bcc8feb37f7e8a071d4dbfd4f3a02c1458ca4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f389fbfe39589cb28362455dc98388cb5f7e6bb95664a51ced670e3c3ae6e4a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:20:51 GMT
ADD file:cb5ed7070880d4c0177fbe6dd278adb7926e38cd73e6abd582fd8d67e4bbf06c in / 
# Wed, 17 Nov 2021 02:20:51 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:20:55 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1230f17f526cb07307d41462355b10488b994e8bdafe0d8f275a405fa3b33831`  
		Last Modified: Wed, 17 Nov 2021 02:26:06 GMT  
		Size: 50.4 MB (50437098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1d365fccf5329e62283deb47a8dcd67f598107ef33e7137895a33336c9aa65`  
		Last Modified: Wed, 17 Nov 2021 02:26:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:d03268d487ecb693d45bee3650c7ae38183a7379ca52b9f49c1a57a1e0563e6f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77ca30cb718fc7b52f867676df720ccb9c63aebc61ee616a2a75c80973b41606`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:51:05 GMT
ADD file:b19cf756330e0e1577062a56604b50597d35a6f4be67ac86210ddf4b4203a32d in / 
# Wed, 17 Nov 2021 02:51:07 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:51:22 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:141c2db3ba99259b105dd1f16b4f6365959cb21d4978470a6bd73ef86ef15d08`  
		Last Modified: Wed, 17 Nov 2021 03:06:59 GMT  
		Size: 48.2 MB (48154304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48905284f0154fbb5a1f034b007920c484418c303eb8c461716059483f5e845`  
		Last Modified: Wed, 17 Nov 2021 03:07:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:857ec3112731ba234add6acc7c99f654b6205a977254c7c28a72811a11f1ae53
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7991117c6a2ec2a3d736bf37515e8f51d193068bf33c3127a13c3d33b14935f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:00:12 GMT
ADD file:d71807613acdf86685f6d640a90e27b7b63cfe0f13d88668ee943aca089d8876 in / 
# Wed, 17 Nov 2021 02:00:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:00:28 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:10acd81022d17f452439d0385615fa066b8f0ddcf3c1a803872eec5bdc6acf64`  
		Last Modified: Wed, 17 Nov 2021 02:16:00 GMT  
		Size: 45.9 MB (45918099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e1f5cd20cbfac21a12a2c5f85395f19795e1327297e1268d381edbdfeb0b85b`  
		Last Modified: Wed, 17 Nov 2021 02:16:20 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:cf9b0e4cd6b2913a0109c7ed39a745b98beb1fff912fdd7aac097757457a3532
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49223214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095bcebb1970bf5d42d757ee6fe38d02a5533095370387311f0973edfac474eb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:40:35 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a142dd68d6b234935186e085ee6ca4d3990d58e29f3bc89f301eb21a3fcf7f`  
		Last Modified: Wed, 17 Nov 2021 02:47:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; 386

```console
$ docker pull debian@sha256:ddc3ba1a187102ae2de6fe8631ed145202973d548100aee1b3505b862a8e4096
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41b940a276ee4669549fd6fc613c98e582e47fc5230b71b9e59028da40afd13e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:06 GMT
ADD file:87367b4870b0dc997a37b7648ff6efa8e42bed68b0573be2ade992c206fbdd2e in / 
# Wed, 17 Nov 2021 02:40:07 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:40:13 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1f740e90292e8fcb22dbbbdbe335252fd87d406cd6e139738853fc65c8bb54f4`  
		Last Modified: Wed, 17 Nov 2021 02:48:17 GMT  
		Size: 51.2 MB (51207728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0805511207a5413b43b826b427a7a9376941b9e9bd25d957367e1c80a15a5c8c`  
		Last Modified: Wed, 17 Nov 2021 02:48:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; mips64le

```console
$ docker pull debian@sha256:90ebd3461ed035c3af383d20f63edda9a8d0f86224eead89f58aa534d9d6d851
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b76fb87ab66c0e20a099accdbfbad84aa8548511fd5bce253b6b33baef6b538`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:10:39 GMT
ADD file:4769a173ec92e69a1b5cd79af0ed018bf150d1ee278de07f4bdab45f55f3c818 in / 
# Wed, 17 Nov 2021 02:10:40 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:10:48 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8c028c43f55209ca75650433b923c8952e16d106529242daad16c3be3efd66a3`  
		Last Modified: Wed, 17 Nov 2021 02:19:53 GMT  
		Size: 49.1 MB (49079535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ca2ad13dd9b55f9a63dd96976f8aca10242a05f16caea721f697193081df3c`  
		Last Modified: Wed, 17 Nov 2021 02:20:08 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:057ded4168f1f20a3ff9f8f58ad3feb04e228fd1898f274419413438afa30820
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54183926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b7aa843f820aa3220b23a0cd2fe8856a0d80670169ffa62b18a0f59277a27f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 03:29:10 GMT
ADD file:fc0d43ba74311deef20b2131cca3a8e86b083624d63560251191adca21417f2f in / 
# Wed, 17 Nov 2021 03:29:20 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:29:57 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:aad6e1fe6f7c56b0e1b5850f40e4fec91ffaed4b6235e730f5c7ff43db397d3d`  
		Last Modified: Wed, 17 Nov 2021 03:56:39 GMT  
		Size: 54.2 MB (54183702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c43e04afb43b19bebd093168c4e86b8f5fccc39ae6edbff703fd549cec5f51`  
		Last Modified: Wed, 17 Nov 2021 03:56:57 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:buster-backports` - linux; s390x

```console
$ docker pull debian@sha256:e46c35ef6233ba45fe3a010267d324dfe9506e77af4d1fda04b8ed26402980ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e5e8c4151155c6da97939d4334448b0033d6949e8801994a6269bef5b15b0c2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:42:40 GMT
ADD file:dc4ee96f81059accdc88a686f80f1714bc9d2f383af71c0d130c08560cea115e in / 
# Wed, 17 Nov 2021 02:42:42 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:42:50 GMT
RUN echo 'deb http://deb.debian.org/debian buster-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:c12eae84d2674466d924a139a276e361afa9f63de21cf77eae19bd94eaac2629`  
		Last Modified: Wed, 17 Nov 2021 02:48:42 GMT  
		Size: 49.0 MB (49005439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00ebbe55196ab0850ea52c63f7f243f11a7857810569ea40aab682f32e81c2d`  
		Last Modified: Wed, 17 Nov 2021 02:48:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
