## `debian:testing-backports`

```console
$ docker pull debian@sha256:262b6894eb108e6f0a734b0aeb1b4b182d1422587ef177a5bd4cf5bd1a91ce1b
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

### `debian:testing-backports` - linux; amd64

```console
$ docker pull debian@sha256:e46896ff48d2bee6b67da729dc11ffd34537a78d296a7d6bffa7d471d7c81345
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52332721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f78602bbc91db4efadef0bd27e8d07f94b8556a4e2fbe3001073e5cc4061e6b`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:41 GMT
ADD file:77b2384f97a0a5676c125b86f783e7ab40180debb7991c6056f1792dc33f367a in / 
# Sat, 30 Mar 2024 20:52:42 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:52:45 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f7635fb521f044eccaf7ecb3cf352ae689043c2d033b3999755c0c9fad1c3836`  
		Last Modified: Sat, 30 Mar 2024 20:55:11 GMT  
		Size: 52.3 MB (52332499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a06b46f3e81e84669133d9a2134071e7ff4748bd3db4faae74478c9a6b654da1`  
		Last Modified: Sat, 30 Mar 2024 20:55:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:6edc4042b50995d83dd277dcc3c5603b72b87d97acbf078e65bcfc6e361d584b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49422419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c7a66ed407afe34b3bd6b45bac684f2278124f117158c73f5617ee49d43ab4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:51:56 GMT
ADD file:a7e1d0726d9802b8f1d1532b43178b8a31c742f59909848e6d46e538c1ca3095 in / 
# Sat, 30 Mar 2024 20:51:58 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:52:00 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:253a3d09b8d130232b6aa8e0a21128e146f2af1990786c97c7a056832cb0f601`  
		Last Modified: Sat, 30 Mar 2024 20:54:02 GMT  
		Size: 49.4 MB (49422198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dcfbf30de2ed90739b607f6f65dc0779cfab02136ca546dde3746709d9b2c9`  
		Last Modified: Sat, 30 Mar 2024 20:54:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:79800f93563cf6da418ea9661fbffe3954629ff8b1ec211c61868496350c5b0d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46920677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60c92916e2437f68fffa4f0655d73b90415f20028e3b15287b8891cae123ee4`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:53:03 GMT
ADD file:7844b5853860dca87da00cd504866ab5b607e94bfce0965dfe3442c41250bd45 in / 
# Sat, 30 Mar 2024 20:53:03 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:53:06 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:877f833a6810386973c7bddd0f1c95cd45af89c924a7259c9d4688fafb2335db`  
		Last Modified: Sat, 30 Mar 2024 20:55:19 GMT  
		Size: 46.9 MB (46920455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15a719b121cf5ea8a9142ed136e464b7bec7d36bc11bfb21dbe1e3b6a96b960`  
		Last Modified: Sat, 30 Mar 2024 20:55:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:927db37b1739f2c5252e71014cbb6287c9626e278aa9991de60fbe4323d3bc69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52193391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07c33a6ece618dff4e6d5f88f6bb12b29b739d94a4e8b132200b917e001a9a6c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:20 GMT
ADD file:fc3581778ead218cf3f2b0cc783c67d5a425cb255a88178c9f2a6f07a1806740 in / 
# Sat, 30 Mar 2024 20:55:21 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:55:23 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b431ee02c5840b16ec0729ce2312ad3bdbd0a4edca10b33678f7132ad29de406`  
		Last Modified: Sat, 30 Mar 2024 20:57:27 GMT  
		Size: 52.2 MB (52193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1828e879c7e06e51da37bd8414c3b0c5939130eb2409f487774f4501e1a9bf41`  
		Last Modified: Sat, 30 Mar 2024 20:57:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; 386

```console
$ docker pull debian@sha256:5e3eb29bb50f5b44afc61f777d85a16c27040a64a7ac7b7c27a222dd57e92ecb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53185135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f1550d5fe66fbb21d2f5883647e347950d1ce77824c0da5cbedeea9eab060c`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:52:11 GMT
ADD file:a505417642edd686e02cb10e9185db4d9440777a6750c02aed6860fc9c530a37 in / 
# Sat, 30 Mar 2024 20:52:12 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:52:16 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:1715ccd6a012eb736ed68688b6bd6c252c9db4457103a427e5dbd7e875743908`  
		Last Modified: Sat, 30 Mar 2024 20:54:56 GMT  
		Size: 53.2 MB (53184915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db3c705b6cc09cc3f06ac97d86ca6f68f58dc133ed2979e75c3258ec02453f2`  
		Last Modified: Sat, 30 Mar 2024 20:55:05 GMT  
		Size: 220.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; mips64le

```console
$ docker pull debian@sha256:dbf868211a024259839b622a2ffa41ff5e46fb69ae5c6a0afa66c91eedbe217f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51411219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f684d0b65200eca2a0e1253b6f954cab6355be81826497621bd36cbd03a5c8b0`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:56:08 GMT
ADD file:d09fca68b7cda9a0d68b4848263ab611a606ae734d4e35b22fe3226e6261b38e in / 
# Sat, 30 Mar 2024 20:56:14 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:56:28 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:a9c60be42dff227d0cbe46607dde9362ad58112f1285931237bf0345956cf677`  
		Last Modified: Sat, 30 Mar 2024 21:02:10 GMT  
		Size: 51.4 MB (51410994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e7c61e034efc47d362c7f46a0ac786d9df71a34fcd6aa334cd81c2aec50dcf`  
		Last Modified: Sat, 30 Mar 2024 21:02:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; ppc64le

```console
$ docker pull debian@sha256:f4d755be2455133e1196a83424a74efe5b183e6ad5b7428679b16542e620b330
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56249744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4190f603199bbb18bb7cf58f76fe5fe996d9a8dbc66b6250bc18874094ce36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 20:55:36 GMT
ADD file:969150af93cca0492ec38ed28e99d751e4328a4b698b0749dba2a7efb2294919 in / 
# Sat, 30 Mar 2024 20:55:39 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 20:55:43 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8890528697eb671e515f58d20d435b6f73354841a85505ed32df7ec7b2749faf`  
		Last Modified: Sat, 30 Mar 2024 20:58:13 GMT  
		Size: 56.2 MB (56249519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec52ae20dc6ca8897688533686c4f818383c67482305635bf3a281a337e53dc`  
		Last Modified: Sat, 30 Mar 2024 20:58:22 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:testing-backports` - linux; s390x

```console
$ docker pull debian@sha256:612547c24cce5f77273500992a165446ffcd19814385fb8629064978ece3499f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51761937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa84e33bd64cfe2faf0453e9b1e3a99865c7f93242b3902f5294b46454a26733`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 30 Mar 2024 21:16:07 GMT
ADD file:4cf8f049784ad79cee791438a36361dd5a8aff4c9cf5401b4f11c9be601b72b7 in / 
# Sat, 30 Mar 2024 21:16:10 GMT
CMD ["bash"]
# Sat, 30 Mar 2024 21:17:15 GMT
RUN echo 'deb http://deb.debian.org/debian testing-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:e5d90e7cd041c17afc4e2d20f0f2e7d0c735bf93ad5a6b4c46768cbcfdc1dee9`  
		Last Modified: Sat, 30 Mar 2024 21:28:50 GMT  
		Size: 51.8 MB (51761714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e4605dad55e05ccd92ba3915b2fb2b02893a16c953f4cf33dbfbad094a77b1`  
		Last Modified: Sat, 30 Mar 2024 21:28:56 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
