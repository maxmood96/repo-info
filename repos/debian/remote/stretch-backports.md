## `debian:stretch-backports`

```console
$ docker pull debian@sha256:b51e5f724ee27426953eadc15d4e5fa50d0b9cb03ef57449fc07f95215486c80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `debian:stretch-backports` - linux; amd64

```console
$ docker pull debian@sha256:a8791eb757b03b22f3c218b0907de0cdf8c1d9feae3acd5f77ceedb8e00d3a5b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45376150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:823b479e761e0f4b373dda4bc2a2cfd0f7e410adb6ed4091bfcfdad937e164e6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:23:50 GMT
ADD file:774b5e2033bb42ad97daa64267a5f041124cc0b05ec0198f1b5578ceea5a48e4 in / 
# Tue, 31 Mar 2020 01:23:51 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:23:56 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:56da78ce36e97a8ba1f860575bb1422d1cb6ab4dade70b06ddf1651302dde955`  
		Last Modified: Tue, 31 Mar 2020 01:29:15 GMT  
		Size: 45.4 MB (45375928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6810bdebf11b2927b3dbc96bc91b62a2efb4301d0ca6d55ba1717d4bfd674be3`  
		Last Modified: Tue, 31 Mar 2020 01:29:20 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:34bbcd3bb34a6997750d766f0e6d0ba71c2e678313c7469b1039e1d39b647f69
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44066674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b59170452b08e754c245011fd40fb0c6fcf1712e7d86ac92ce459927cfe970`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:29:01 GMT
ADD file:5a406f17e0981025084e19ed83a5deb90ebcba048fe641c8273f340add75cb3f in / 
# Tue, 31 Mar 2020 01:29:03 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:29:11 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:442790510f4830e8d231c31971c1ad175b7d7fbf094edfb7914e6154fcd31434`  
		Last Modified: Tue, 31 Mar 2020 01:36:31 GMT  
		Size: 44.1 MB (44066449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419904601219ed90bcb0ed8383e7415bdcffd5a44fca758d7ac7dcee9fabb3d6`  
		Last Modified: Tue, 31 Mar 2020 01:36:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:780033a624312cec4f2dccbd664d2a13d60ad808efaa7a261916cb7cc43fdd94
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42100315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18361bb3e738f2ac427ca100c6fccf0a54509e4bebdb015bc16c0eb7d9d75038`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:52:24 GMT
ADD file:b047b0c4dbfbcc048385195e807283b9386c4aac13a4841112cb3f76cd932b06 in / 
# Tue, 31 Mar 2020 01:52:26 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:52:34 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:eb3768893937e6b455f98cd8db65949a6aa5c54ebd94fca3039af9833187ce10`  
		Last Modified: Tue, 31 Mar 2020 01:59:52 GMT  
		Size: 42.1 MB (42100090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08347b8a9f291282dd025db1212ee72883000f6f02e835f38567809f994a547`  
		Last Modified: Tue, 31 Mar 2020 02:00:00 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:82afb6153b55f21615df61dd1810fd67990ede0d8da22f6220ffcc29b9077633
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43158343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ae8a023fe9cbea514d979eac16cd8de2c5877aa3db1ce14e216d542bd0315`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 02:08:11 GMT
ADD file:ab80e35f9496440fac439083c9c9c18cd80521039d4bc4f4082e8e84a5e9fcda in / 
# Tue, 31 Mar 2020 02:08:15 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:08:27 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:84582781a9f06ad84225307f9cf89d5f77f6e5610281e6ca088fc8c2e9a1d027`  
		Last Modified: Tue, 31 Mar 2020 02:14:13 GMT  
		Size: 43.2 MB (43158116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec7efa6b4f7ad9f12cf24a8c089283fc7735c3e8e65cd32a9a82301eaf5d8e3`  
		Last Modified: Tue, 31 Mar 2020 02:14:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; 386

```console
$ docker pull debian@sha256:604873927003b73f625f920471bf40a3f0eb2feddacdc0a8d0fbd1bb7117c971
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46095407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3784adef19b08f04c113a357082a24bc184504693c0feb5997e908252861231c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 00:42:34 GMT
ADD file:a2d15d4f5721611194d2e75c068cf76220a1fd273b28e60afc9d97c41920f37b in / 
# Tue, 31 Mar 2020 00:42:34 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 00:42:39 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e23f42c0de4ea650702adc216b9d71349a24439e774c0bbbb00d2ad19aa304df`  
		Last Modified: Tue, 31 Mar 2020 00:48:31 GMT  
		Size: 46.1 MB (46095182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff5ab10291db4135562244fdcfd6468d814526491f06496ebdf1ab460ee92adc`  
		Last Modified: Tue, 31 Mar 2020 00:48:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:b0abc62c16c2bd88160f6a8aa38913c8184c89d47b6dd40b696fa30e994ce0d2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45647363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d38d91efe927c886ebef25fe291a7e9ad65b8b75197b511de56e566f269fd6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:36:08 GMT
ADD file:88dd9829c8f6a5ba7164ab347e4b14c986122f77fa3881b5b5f9bd34f8e0a794 in / 
# Tue, 31 Mar 2020 01:36:13 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:36:31 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a7f28865f7aedbe572d508cc57c37cad5f147864f7c67c67a38458e070687420`  
		Last Modified: Tue, 31 Mar 2020 01:52:56 GMT  
		Size: 45.6 MB (45647140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53f2d3803b28074141f348ae6ce49cbfe9a8f371b1766759c113e43de3bd5752`  
		Last Modified: Tue, 31 Mar 2020 01:53:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:stretch-backports` - linux; s390x

```console
$ docker pull debian@sha256:d3a4543173e9ef97cd6a8bbb6a2c973bbb8d5edf8263dc7c7a750ed1d01605f4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45233091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:442030066602db8e8efbafa91a67eff11073ca909412ac669879a8ca01209141`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 31 Mar 2020 01:10:18 GMT
ADD file:4b10f5f6f8f327b6ad71def930275eb5f518828e8eb19f79d20712e112ca35df in / 
# Tue, 31 Mar 2020 01:10:21 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 01:10:26 GMT
RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:32a0ea7e09635bc86f70dd4db2b929ad05b81856f2418c0f482b647e3ec3453e`  
		Last Modified: Tue, 31 Mar 2020 01:14:05 GMT  
		Size: 45.2 MB (45232869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b056e1fa8e5c40e29e5eebad558c413eac7483db0b0dd64c5d14583f9ecbb379`  
		Last Modified: Tue, 31 Mar 2020 01:14:11 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
