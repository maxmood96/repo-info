## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:3319d7159a1f4aa79f049d1741f469c9a4e1ddb6140883d2cda6bcd718f2f672
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
$ docker pull debian@sha256:239d9e4eb78c851a2a66710231b14b6be0ad7c8c01dfaeba15780066998a1438
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50437340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1a14faab04137586c9950be2c3f38ba3b6881bb6527989351a112e8107d763`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:21:30 GMT
ADD file:aced752439c3c72517c140929de0ae8f976ab707d1478009d82941c990f76350 in / 
# Wed, 17 Nov 2021 02:21:31 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:21:34 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e48a3e484caf9b71146dfed9e8b197f3cb75d6a16e3574444620ce01a70aff44`  
		Last Modified: Wed, 17 Nov 2021 02:27:27 GMT  
		Size: 50.4 MB (50437114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deebcf83c54247ca085f33e534d83db7267d76a1898270c338c0d42d95d57fbf`  
		Last Modified: Wed, 17 Nov 2021 02:27:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:daa680dfd2e73899f7e7b4ea9f11e01784e1d514446e7c54be6711ae93232eaf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48154478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d5779c161b2592b12af076c1f38a41355041b35489be23353ce4b0ea09ad30d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:53:02 GMT
ADD file:5be4d0bc23a41d7eda9d1dad80f038f9b00d3586628cceca67b22a7ad1cef857 in / 
# Wed, 17 Nov 2021 02:53:05 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:53:17 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:468846ae46a4adb2e0d8890885e5b310f36a4aea4883dd3803adbfd8287b27e7`  
		Last Modified: Wed, 17 Nov 2021 03:09:40 GMT  
		Size: 48.2 MB (48154253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570e89d8a6851c1151cfb70c18f66cd2356c846d8b9a025690a0df8414b7fb10`  
		Last Modified: Wed, 17 Nov 2021 03:09:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:d8eab25cdec6ee0208542e2cd49d649065538a83ba8f49f840a83d1f8042b4e6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45918333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:727832e9bf3b5d7eafbef22872f4e50bebfd9b313e444d675f9c682eba7ae018`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:02:12 GMT
ADD file:23851ef44d699801f834722aa6530215ac3a6dcd500c76d1bdcded99688a68d8 in / 
# Wed, 17 Nov 2021 02:02:13 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:02:25 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b959e8636c3fbc4fbcb87bab1fd1c0342f5c73abfb922f435e0607f1c1937f03`  
		Last Modified: Wed, 17 Nov 2021 02:18:34 GMT  
		Size: 45.9 MB (45918108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32fad563492aadc2b788336a7156f6a35255f2134e6511e46b18aa2e72f3edd`  
		Last Modified: Wed, 17 Nov 2021 02:18:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:61f740b7821dd406e23e93d0a8feb12f2ece0589ba5b792fe26a25950ecaaac9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49223228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:784da462fd513a639ea87ed9f4f94362ab272c1d2a6c5a53641dda3672380cc3`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:41:20 GMT
ADD file:0bf72871c9dc02db2e698d59b049f2c2e2006efd248ac786ac9aea42bcd22fc9 in / 
# Wed, 17 Nov 2021 02:41:21 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:41:27 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:2926301144acff341799afd8cde6828df5c64ca6be41a692ce22a8eeababdfaa`  
		Last Modified: Wed, 17 Nov 2021 02:49:11 GMT  
		Size: 49.2 MB (49223004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24cf6ea5a67f105ab3701247bd2d44a1b8cbb48f1108d960c64e7d2e838ba386`  
		Last Modified: Wed, 17 Nov 2021 02:49:22 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:4aff0a338465244a0f98eb776a2037e55ae4e333e35c5bb2b3d618afac6e5ec4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51207961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa9433d10245875e043ec67c0dd73f2d2f62b8dd30d97ec314d40735c6b2423`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:41:01 GMT
ADD file:4d619a3e402494b6b2b7078d2900116a696c6229528ac7e0f43d4718d9282fee in / 
# Wed, 17 Nov 2021 02:41:02 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:41:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:262b40fd2e74c9a9af1338cd432d8a2f67c4181745bf6a64e1720132db04dc44`  
		Last Modified: Wed, 17 Nov 2021 02:50:01 GMT  
		Size: 51.2 MB (51207735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb174e8d6e29cbd39def53eaf7e397dd0b9dfa8518d41e0c5a1cd5c17a090e6`  
		Last Modified: Wed, 17 Nov 2021 02:50:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; mips64le

```console
$ docker pull debian@sha256:cfd66a4e0de2ea48998174579c0c2d604abea656b038706f6f3533e0ca318e52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49079735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c0ef77ef491b866f95985460bd355f69e20527ae3a0c33f2f1bf6be9abedfa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:11:31 GMT
ADD file:3f62fbdf824f2fcd14e636dbc1bd299b45af61be75ce88c29ce65ab16c3fbe9c in / 
# Wed, 17 Nov 2021 02:11:32 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:11:40 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0811a00b03aec1e2055c56152922ac2f7f4fdc9ded11878e6fb79cb05c66310a`  
		Last Modified: Wed, 17 Nov 2021 02:21:17 GMT  
		Size: 49.1 MB (49079508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9164b9cd9ca845163f611db4dea3f0b203ead603f5f04ecb35887d98590fbed4`  
		Last Modified: Wed, 17 Nov 2021 02:21:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:ded4dfd1da929e17b696a0ce766e6dbff701c93e9cde5ec20ceef8492562f4d3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54184003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abf55232a6aba6d7750abbb9a677598ee413f4ab0eef90ced53e44c88355acb0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 03:30:53 GMT
ADD file:fb62616778cd378dd7e27257d6690a397d27b22aa7afa78026f5f0edb0c26087 in / 
# Wed, 17 Nov 2021 03:31:14 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 03:31:47 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4c0a5998b10e435c4caf5a1b3d6f33eb49ac12985b9e77464ccad3513447823c`  
		Last Modified: Wed, 17 Nov 2021 04:00:40 GMT  
		Size: 54.2 MB (54183775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cc44c649c5811ae3d8fbf91f8ceb4e7225829d136a0ea9efd368b0630a8ae8`  
		Last Modified: Wed, 17 Nov 2021 04:00:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; s390x

```console
$ docker pull debian@sha256:22e6acb44277f5fc96883b016d438c149412434c4c8d4de2a961a7b5d138574d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49005646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8090595779a06c91b5c5ed0c0302404e3d40f696fa65d1f14c03051480e4cfc0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 17 Nov 2021 02:43:11 GMT
ADD file:8093c4a2da0918a23f3506c7248de0407ee728c18fa9f43d6e6bcc4c1bd13691 in / 
# Wed, 17 Nov 2021 02:43:14 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 02:43:21 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0fec2256c1fde808b8caa285d6c8df9138e9318b933d893a2ed591acdb766c02`  
		Last Modified: Wed, 17 Nov 2021 02:49:20 GMT  
		Size: 49.0 MB (49005421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b6eb6b9bed02316d5347909404146eab77a4b65294d5f790fac5b85392c653`  
		Last Modified: Wed, 17 Nov 2021 02:49:27 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
