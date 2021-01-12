## `debian:oldstable-backports`

```console
$ docker pull debian@sha256:0b0a80edf98298e40673b6e38bfbd6190743dfe164aeb3c5db997954b066d728
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
$ docker pull debian@sha256:a6775d49d51fda57ee44ec1142ee4872ffff2c379d1ae57c9925b8a55ca4d0f3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45380253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2791a0818b5428d24dc1f11a2614bb141d1b8e3c505193cc8aa406cc11fe979`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:33:49 GMT
ADD file:16639add5e8efcaa44b7f7267ebba76570a2ee4c5970926c8399389d38097ca1 in / 
# Tue, 12 Jan 2021 00:33:50 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:33:55 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:7385e72b0868aad6973d1db6cbb77062acce32f56cf50c9b3a07ea75ad617785`  
		Last Modified: Tue, 12 Jan 2021 00:40:52 GMT  
		Size: 45.4 MB (45380029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09f64bebf0e950a58e93259c1aaf80fdd207f1e2466d95833dc7c23529f07dd`  
		Last Modified: Tue, 12 Jan 2021 00:41:00 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v5

```console
$ docker pull debian@sha256:e69be02ccaabe3d9d298b4a168c921782c81da39d78bd9dba5c9c108dc9b6a38
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44091670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60290556f2a2ee5483f390ba08a767acd1681b98ff247744ad9afa08e28080f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:53:10 GMT
ADD file:8348d6f8b4abdc5a4a777909b2f4b4b368b3a18d9d91d4869e7377ebe4b041fc in / 
# Tue, 12 Jan 2021 00:53:12 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:53:23 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:4a419789c26dce5efc903f1cdb80fca5e64cf3766895e80c10714592329977a4`  
		Last Modified: Tue, 12 Jan 2021 01:02:35 GMT  
		Size: 44.1 MB (44091442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95eaed9e083eccb8fbbd0485c0e4fb886233295b0deb88cbef3bcdffb34dd9a3`  
		Last Modified: Tue, 12 Jan 2021 01:02:46 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm variant v7

```console
$ docker pull debian@sha256:33745a4375be6a5b2e854e9fd9c90b977fc456556eec21614927bf2a7a11c7fa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.1 MB (42120143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90ecf46ca167ca1948abf9193386fb4c0ac52b9943eb835fb8569576cbaa045`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:02:52 GMT
ADD file:5f49e7ca78da03d70a348da9007ea28d8e523bdb79b34aca387ba5b93fe3cba2 in / 
# Tue, 12 Jan 2021 00:02:53 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:03:07 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:989d6db68b8c12e18dc6cc5379cba2ecfc52ec4bc2e78fb4fd82f3308cb63aef`  
		Last Modified: Tue, 12 Jan 2021 00:13:05 GMT  
		Size: 42.1 MB (42119915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908d1ac102ef53be9d9d9c98e3c130b9dbbe16da4e9a4b768fa61ad7918c8797`  
		Last Modified: Tue, 12 Jan 2021 00:13:13 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; arm64 variant v8

```console
$ docker pull debian@sha256:29ed018e27082a301d47c9a7e5bdfca0f0dd8e23b9d01932e6103fedfe6eb857
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43178292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36109d44959f693f567a4bcd00a1f01441d25e7b9f2532b35f4274a7864f1fe`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:41:35 GMT
ADD file:ff0aa17acc0ceb39dac9d723dbbb14d558589c19737dacc85d918367147c2be6 in / 
# Tue, 12 Jan 2021 00:41:42 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:41:53 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:0d2be31b468d55ecee2b985116b5223dd30733d3286e69fcf65dccb7fa4a8ad5`  
		Last Modified: Tue, 12 Jan 2021 00:52:21 GMT  
		Size: 43.2 MB (43178064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e78ca67a956ea148a22556b6ae261ec38b3b7924741c11235c1092dcc3b3b753`  
		Last Modified: Tue, 12 Jan 2021 00:52:37 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `debian:oldstable-backports` - linux; 386

```console
$ docker pull debian@sha256:0fbeabf198d25d6e54641d76e028fe3124c4aaaa88020b9c1bdec0d38b64ed49
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46097799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0bde61cf198723de489d3c4caf9c221039aef73a115c197fd6c8f49e1b3e69`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:40:41 GMT
ADD file:5d768e450ddbb73846f7b473c61acabfccfc6d00e665a662d9a61bc9017fa21a in / 
# Tue, 12 Jan 2021 00:40:41 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 00:40:46 GMT
RUN echo 'deb http://deb.debian.org/debian oldstable-backports main' > /etc/apt/sources.list.d/backports.list
```

-	Layers:
	-	`sha256:b35cf3999ded14530b30d096247f98c5c522e6acf89f87b447042a71095eb078`  
		Last Modified: Tue, 12 Jan 2021 00:48:28 GMT  
		Size: 46.1 MB (46097571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2192e8a9f7b486677d19cd03b1c749778ed02bbe5e43df257ef0543db43bc53f`  
		Last Modified: Tue, 12 Jan 2021 00:48:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
