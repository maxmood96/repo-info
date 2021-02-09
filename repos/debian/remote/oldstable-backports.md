## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:e4ecf49c71760dc38a19a8b642b2ebd81deacc9b4adf3890838d0c5b9e71cb18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `debian:oldstable-backports` - linux; amd64

```console
$ docker pull debian@sha256:ab2a9a76909b0fd257fc573b748a69950dfe6a5ad92dc9fe0ba323404c487a31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f61ee9f9dc432fc301e772f6180125be930b84c2beea961c352b5281cb37e93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:21:55 GMT
ADD file:20bafdf4d25ae106b39228240d08ac69b3a06f8fcfbaedc8caa02f9472b6d423 in / 
# Tue, 09 Feb 2021 02:21:55 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:22:00 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f64678c29c7781407d12306e9dd4b62e6507892dcbb83d9ea991c566af90deb8`  
		Last Modified: Tue, 09 Feb 2021 02:28:01 GMT  
		Size: 45.4 MB (45379902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62fa409cce993e2b2fab178a41c20fe51c9db260a4e97e2bac11ccf4da520c6a`  
		Last Modified: Tue, 09 Feb 2021 02:28:06 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:dfd62ff0730767d49f123ca95e2161d9a9b8f13594648a138b34cce5a64221ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8f2a5feee5fb1b31cf66170fd10c20c44586743d2c9023debbed2cd5f7b1dd3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:51:56 GMT
ADD file:266488cb20206b2653ab05c1432872149ea823aebcb5f56b2cf4266032ca46d2 in / 
# Tue, 09 Feb 2021 02:51:59 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:52:08 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:fbbc03ca06e713a9754c68b8436b49c1a3231ac3250f73de263519370205fc82`  
		Last Modified: Tue, 09 Feb 2021 03:00:53 GMT  
		Size: 44.1 MB (44091484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fee09f8ea91a954098077ae029bc3dbcbe381cc1c1b6a7b8ba1a542acd8b415`  
		Last Modified: Tue, 09 Feb 2021 03:01:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:7b3bc7b827c107dc441964fa19c844dd910340e2e8c5d542596bc75da5425b18
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ca279180c43149a9af6cd36e43504b337276b39f0740b9c32d534f998af314`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 03:02:45 GMT
ADD file:1fd88527508577ac6d9e2db6410da4136decce5138e51edd778c603e5c0d047c in / 
# Tue, 09 Feb 2021 03:02:48 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 03:02:57 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:f53be56e59ee3f6b878378bd1f05d5c4442fe7737638ed763393be7e69a47a9a`  
		Last Modified: Tue, 09 Feb 2021 03:11:28 GMT  
		Size: 42.1 MB (42119948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430e1b931eb5e7e7f2baf9413b7441ceaf177557dd0846a8d342c7499a42a5cb`  
		Last Modified: Tue, 09 Feb 2021 03:11:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:f3fee02743beefce4685efabdc695e181b8685c5c3e05b267bdf3d213a341712
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43177869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:880a3e427b8f8cbcc71ac0c96e9b37f73c11a75b9f8dff598a57e17135de068c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:28 GMT
ADD file:d04376909451e764223ea2594ce052780641f4d5cc4fbd06d33741f80b17ab68 in / 
# Tue, 09 Feb 2021 02:41:30 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:41:38 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:612b436904ddd9ff24be7a3801278dd7c6ca8a0ab14d40826c1ba6e4ea84b66e`  
		Last Modified: Tue, 09 Feb 2021 02:47:47 GMT  
		Size: 43.2 MB (43177644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ccf4642581c98c0b490fc2c5191f33e673e7dba84e854b71d55e2c8f8bee0f`  
		Last Modified: Tue, 09 Feb 2021 02:47:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:5602fcff36d87564a6365eb86d66d7c111eca85807dc347fedfc725b3c4852af
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff09eaefae81cde600b92afd657d1068796b318133138060f3f8060d101b7469`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Feb 2021 02:40:50 GMT
ADD file:5522a854d2d77afdd29a13621b4705e6edd7eff274647c038fdcb05a1277bf4c in / 
# Tue, 09 Feb 2021 02:40:50 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 02:40:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:8f5abe6b821192422ef3001db0af90f54103f04f2388216df8d7858287cb8b4a`  
		Last Modified: Tue, 09 Feb 2021 02:47:26 GMT  
		Size: 46.1 MB (46097647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d950aa20e6f9bb2b6e3ed400dcc61c9e9b6c59fbee050835dd86582342758a00`  
		Last Modified: Tue, 09 Feb 2021 02:47:31 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
