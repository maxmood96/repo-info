## `buildpack-deps:mantic-curl`

```console
$ docker pull buildpack-deps@sha256:3686f11891103137782befbcd67f50433fbfc6dd55a038b13a14fe2ca14407ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic-curl` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:67c5c72393daaa311813c147c29b11e206a74eaa529bedf9f39eb69ba579bf1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41539391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:600cfbf723eb7c8bf4ce8d3f5a932754804867c8248e234b61709d417cfb2fa3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:50:42 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:50:42 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:50:42 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:50:42 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:50:44 GMT
ADD file:592c8f21973a80f096ca38aaf5ef478d80f666517a169bc638ebb325f5ae07f4 in / 
# Wed, 12 Jul 2023 04:50:44 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c57e6f7e53eccd34261640d6f245ad38a4ff7cc54ead279536b568d836363ae4`  
		Last Modified: Tue, 18 Jul 2023 01:49:46 GMT  
		Size: 27.8 MB (27758391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70262639a4fd505c867f716c40dd85135752950cc1aa365725b9e2967d66175a`  
		Last Modified: Tue, 18 Jul 2023 01:49:45 GMT  
		Size: 13.8 MB (13781000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:271f5554f255b23ea62c0fb8cfa0036490f85f03075208f4ce854759b22af254
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37953265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f062601d79881dc384843361649ee83c718f46921d65ae0b7e8eaea6f583f3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 28 Jun 2023 09:16:41 GMT
ARG RELEASE
# Wed, 28 Jun 2023 09:16:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 09:16:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 09:16:41 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 28 Jun 2023 09:16:48 GMT
ADD file:53ef0e936c198583128a468b64a8223b792a28cbd74935a7aaa5fa145b4053b4 in / 
# Wed, 28 Jun 2023 09:16:49 GMT
CMD ["/bin/bash"]
# Tue, 04 Jul 2023 06:13:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:20af62948d2ad360ef116fe2eef1820df7f5aeee326beae2e81efcc6e366f665`  
		Last Modified: Tue, 04 Jul 2023 06:25:22 GMT  
		Size: 25.3 MB (25270588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ac3606f55aa9aea708e379f37c263f56752be04b8642f50a6f4c8046333a8`  
		Last Modified: Tue, 04 Jul 2023 06:25:19 GMT  
		Size: 12.7 MB (12682677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:10bb9957c553ac1c04cab432f23e71fd04ef05d3f508e6d3dbd79575f22c2155
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40480695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24c82d9a81946878d92e5085da84d06a6e9a112da2626ae0b6e6b6f5b163b5eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:54:30 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:54:30 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:54:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:54:31 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:54:38 GMT
ADD file:6eb08bb754e74bd297a54d5c56c7622fe3945c0e013d8a48b8d85b09f1818099 in / 
# Wed, 12 Jul 2023 04:54:39 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4f4369a81c2a2103bb37c89ff5ddb71caf0eefa6abc6ace3a6312b114b1b43f4`  
		Last Modified: Tue, 18 Jul 2023 01:51:33 GMT  
		Size: 27.1 MB (27116407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9605105b68496ddcb5871d9313b51b49ff984efaf7993f0d2e84539e1fd35b1d`  
		Last Modified: Tue, 18 Jul 2023 01:51:32 GMT  
		Size: 13.4 MB (13364288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:421ccc57b89ad1944922fa394d2470b2be35a62b46beb5fa6f1f41f2c55d9fd8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47875497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ae0c1a5f5ac2b746df491ff907a5d5dac297aa1dd8f05331e7fad11dcddb89e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:53:28 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:53:28 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:53:28 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:53:28 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:53:31 GMT
ADD file:7028e8b5bb04424a3fa537fa5b5a311cfcaf1c8b6f321b414b40ee0388d0f9e0 in / 
# Wed, 12 Jul 2023 04:53:31 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:52:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eaefff58e8d715237ca48dbc24624ab97d73780134b6abfa9397a3fb107c7847`  
		Last Modified: Tue, 18 Jul 2023 02:02:03 GMT  
		Size: 32.0 MB (31995451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3142716ff35072c411419b141a83ce524bc1af91e86195277f4ca49673988b19`  
		Last Modified: Tue, 18 Jul 2023 02:01:59 GMT  
		Size: 15.9 MB (15880046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic-curl` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cc5d376a0d42b93c0b1aeb249929f492d1f04f9657bab633903b45c4d26539bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.4 MB (40360013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb0b4528866fd72155a4910ab9744bcddf0bde069e7a9dba2084fe2d14eceb5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 12 Jul 2023 04:53:32 GMT
ARG RELEASE
# Wed, 12 Jul 2023 04:53:32 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 12 Jul 2023 04:53:32 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 12 Jul 2023 04:53:32 GMT
LABEL org.opencontainers.image.version=23.10
# Wed, 12 Jul 2023 04:53:34 GMT
ADD file:878995fa3a12c9df0a99fc88605932ffefec3e772a3c4ca89fe0c0aaa7dee67d in / 
# Wed, 12 Jul 2023 04:53:34 GMT
CMD ["/bin/bash"]
# Tue, 18 Jul 2023 01:13:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2b8f6b9cb3947ae25987d6e3685dc9709178b596bd7bf0d7a84ceeba23a2073`  
		Last Modified: Tue, 18 Jul 2023 01:18:14 GMT  
		Size: 26.3 MB (26322139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b736a5889ac0138557b62eaa679858540efdff47fa4079b2d261d5d981a0b7`  
		Last Modified: Tue, 18 Jul 2023 01:18:13 GMT  
		Size: 14.0 MB (14037874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
