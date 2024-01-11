## `debian:bullseye-backports`

```console
$ docker pull debian@sha256:8c6288582b2bfa4fdba986c1928b714f5bca71922dc734a901da499b1b484788
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
$ docker pull debian@sha256:9f4ac8f9c2346f115172ff2dbb00e472937e7ee6bf8fdc0c330ef01f0a0b6a39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55057948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6526714fe1cb42a2ec61852babfebbb34ca2fd49768346f45f1498863e114b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:04 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Thu, 11 Jan 2024 02:38:05 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:38:08 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cc6f262ab33476327eec84e8b8dc3d50f25489adecc54ad9e601d023e2552f5`  
		Last Modified: Thu, 11 Jan 2024 02:42:58 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:14111412f8c5fb4be563abae66453a3826e9e1d7a18132545161096bff751e3a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52562733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f46bdb7a2fb838ad00d6ab0e339d15dea19cc7c411be4e5b5b6e641798169e67`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:49:11 GMT
ADD file:a5224163b267c4b112f96005ef36619be78d0b949e20d9008f94efc7116f9605 in / 
# Thu, 11 Jan 2024 01:49:12 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:49:19 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8600a8817f4f0136707c29239c933cdd333774f1c11cb22b584b1a8aeb8dfc22`  
		Last Modified: Thu, 11 Jan 2024 01:54:27 GMT  
		Size: 52.6 MB (52562506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0f52cdbd9dad3277fbbd65069b209ab0424d096996e62343a9eecb33c82dd2`  
		Last Modified: Thu, 11 Jan 2024 01:54:41 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:0543bb011da0d509a54e002d682bae932ba3c4f6c885435271ac05e60f04df5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0323b687392fb9b5d76ecc95bac85ec983116b1f4ea448ed747b61b7279c2f6b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:21 GMT
ADD file:06c355196a858f2594c761bea3314e053018c78a4b06eabe168db940f6c18e26 in / 
# Thu, 11 Jan 2024 02:42:21 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:42:27 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:6c8fc6a3ed50d9d1c829e556b5efd4ca23cd5d51d5dcdec2a7a70b583673ef89`  
		Last Modified: Thu, 11 Jan 2024 02:49:02 GMT  
		Size: 50.2 MB (50215530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8865bb26e8d6804918a927ac57e4e70bdb42d0eb36216a19b7e54c179497b20e`  
		Last Modified: Thu, 11 Jan 2024 02:49:14 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:6da045f46f02a11b18655ee7790b1acf1d2eed7fb9dd9a88025824b3982ab7ce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53708073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1f9b74ef125a1ec2fca710a9f987d5e384380780cef1ad1c285acc2c723be07`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:40:51 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Thu, 11 Jan 2024 02:40:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:40:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36424970d096e0889a1acf4e36159ef5e3fc54bf31da1992038ab0e86132cd5`  
		Last Modified: Thu, 11 Jan 2024 02:44:38 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; 386

```console
$ docker pull debian@sha256:1a71d4da5a44adb174e0e4aa0e2579450ef1e6dd4139fd9bc21af580547589f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56046612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adaafcfc684fb9aace0d09eadfeab40b308c3909cf1ee07ff4339944e7109689`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:50 GMT
ADD file:5ec37a8451203256eba8b114f21ff297f9b2e0b420ec7f0c50658a448ffc8f7b in / 
# Thu, 11 Jan 2024 02:38:51 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:38:54 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:9b04188f89c4a7eaa549c59c16834ec81012244afac6c52196bafd2cd4486602`  
		Last Modified: Thu, 11 Jan 2024 02:43:42 GMT  
		Size: 56.0 MB (56046385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afa387471522128660d6b0ee2992466796cca4eb2d185e8cd123c7375dfe1dd`  
		Last Modified: Thu, 11 Jan 2024 02:43:54 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; mips64le

```console
$ docker pull debian@sha256:2d310c1b04f5db7e918a3ba4274d17cef5fb59412a9bae34613682b9e981840f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53289103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df59ad213c8cb341e7ee809441c5c9a8958ba442083534e63380d8c11b3f8fb6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:12:20 GMT
ADD file:624f588d8cd5ac8189fd789968263b87196e86dd1d90debb6c5261b515ce80a4 in / 
# Thu, 11 Jan 2024 02:12:26 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:12:40 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:80f37a7fb2daee9d24c2a15489b4104fd20747297db13799a90f5f67e3a79154`  
		Last Modified: Thu, 11 Jan 2024 02:23:35 GMT  
		Size: 53.3 MB (53288875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96bbcac0c7627e9f3b5d35a65a6d3744e2f58c532eb9771d7da298ce10f381ea`  
		Last Modified: Thu, 11 Jan 2024 02:23:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:de72d0ea6e35991a6f0a3450d4015cde2917bc6b2a7c7a82ae900668e27fcff5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58929890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa8fc8a19d695b7d198335e3a215e11d612792d2c6812b573ab90afa93ee34b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 02:34:41 GMT
ADD file:cb900134161e1d051fb57c4a488efa9478959953f2773baa8a90b13198589a81 in / 
# Thu, 11 Jan 2024 02:34:45 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:34:50 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1b9340c192fedc0211d4cda28f7a01e9ff3be108c42783e576f4a366c373f30b`  
		Last Modified: Thu, 11 Jan 2024 02:39:48 GMT  
		Size: 58.9 MB (58929662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3930073574e3f0879e44f56d9acbba500b0b8c91e643a8bea72d192281282727`  
		Last Modified: Thu, 11 Jan 2024 02:40:02 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:bullseye-backports` - linux; s390x

```console
$ docker pull debian@sha256:8a0931b82dea7a1cb8dbe15bd9b00dbb1ce2c7e6a77f61555127bedb65d4a343
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53296350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28cc7604fe239870ffbd5816f80d3b8b46b2bd6bb02e444864d5fe0d8d2fa066`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 11 Jan 2024 01:45:23 GMT
ADD file:9ddcb5238e539e3b1fd8032aecf5e40f0b8b8162e6d045fcd58520db01e93296 in / 
# Thu, 11 Jan 2024 01:45:28 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 01:45:35 GMT
RUN echo 'deb http://deb.debian.org/debian bullseye-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a1442bb0c8abfd050e8bdb2270126c2f24402a8c57a00f8229c40c2a35253665`  
		Last Modified: Thu, 11 Jan 2024 01:51:04 GMT  
		Size: 53.3 MB (53296125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1a7193edb0b963159e7da45992198bb708f40a0f91365da767e8b9ae0c460b`  
		Last Modified: Thu, 11 Jan 2024 01:51:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
