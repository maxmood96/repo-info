## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:9be0d776d126e43dccc268be4cd1007c71039f45c332e8541a27cdc8388cb3f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:resolute-scm` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:80c2ff87631696f8c46034ca8d22bf3d97def420ea82675a9694c731cff372e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.3 MB (101269481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5f9128527d4723d380a97cf61d1b5ca3a36ca9a2217f4e19b35139110bfed07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:28:38 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:28:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:28:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:28:38 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:28:41 GMT
ADD file:55d8d7c2a599eebdadf029d609185a93b70e5c572fbf864d8e1dea8ca32c7e8a in / 
# Sun, 30 Nov 2025 03:28:41 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:11:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:ab1cebba4171ff5f2efb3092f20bb54ba4f8853e67ae7ba36b66c426fd17d4b4`  
		Last Modified: Tue, 02 Dec 2025 21:29:21 GMT  
		Size: 33.8 MB (33763754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db10505684265b8f15b7389af79a333e81deff06c492e0c86a76684ac37bc564`  
		Last Modified: Tue, 02 Dec 2025 22:11:39 GMT  
		Size: 19.4 MB (19408148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecad741edb8a7bfc0a31060fb84a145b290196acbec4e0ab37b15a7ef2e8d5c6`  
		Last Modified: Tue, 02 Dec 2025 23:11:32 GMT  
		Size: 48.1 MB (48097579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c8ccae2a15332e72b26fad4fd8800bde460e1900ea8ccab940283153bca5f6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5760040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bced8f6464d0a68b0df91f50552251d5d68655c0dea71a0ad30d768758d10d`

```dockerfile
```

-	Layers:
	-	`sha256:78abea08949da9e8c2c7e4a6076de4fdfdad731ec6adf7759d7f41eae9f2649c`  
		Last Modified: Wed, 03 Dec 2025 02:20:20 GMT  
		Size: 5.8 MB (5752759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbdf6ac9db84d31f286f890da0dcc211eff8f367fdffd8d2d563d26053f16d62`  
		Last Modified: Wed, 03 Dec 2025 02:20:21 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:93abde019078070f94eda6ff2fca0aedea662d7dd3d9ef313d3325aecd06dae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99495058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc13403cf9dce3a19876a0aeee87f90dbd9d4906bb03871c7138dde824582435`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:55 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:55 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:31:00 GMT
ADD file:9003dc9541ce76045dd67f0ad2d95c2697e3b7155bc6abaa06ebbf38b78aa407 in / 
# Sun, 30 Nov 2025 03:31:00 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cd71ce16db91fba8d9cd0435979699051c3f118fd7c402d7cbdc6eb32d240426`  
		Last Modified: Tue, 02 Dec 2025 21:30:00 GMT  
		Size: 31.1 MB (31147436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148d15adde59bf29b7e8735e2ca69fe70d44a2559de9882a34bf8c8ed08114a7`  
		Last Modified: Tue, 02 Dec 2025 22:11:34 GMT  
		Size: 17.8 MB (17756410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1a9c5eb4062359ec001f06df08977ad317de1969c45cac1858b9e39fe7e85a`  
		Last Modified: Tue, 02 Dec 2025 23:12:20 GMT  
		Size: 50.6 MB (50591212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:ea8ecf465a1b33eb18e367223e94e0f5ae15d7b28b31587252d3081c956c6d6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5760600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3349bc58d94e71d55bfac19d0af1e597431c8eb2f19a2b0f02651585d610db95`

```dockerfile
```

-	Layers:
	-	`sha256:1662d91d876bd5b5f8cbcd7e2bbca340ed542570e9d677e000e484eef33de4ee`  
		Last Modified: Wed, 03 Dec 2025 02:20:26 GMT  
		Size: 5.8 MB (5753255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bb1d9970e92be2459c3cd2d104ace145d6577a8036ebb5c4e58ab5c27d50819`  
		Last Modified: Wed, 03 Dec 2025 02:20:28 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a9f62ebdd4c5b2bcc8ccef23d357252c99e48e0ac56ff18eda7e317dc830b7fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.0 MB (99996133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66af0f62a2d37fcace36ba505cd320427f42aa6eb2672903e7cd12873d9aa862`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:30:15 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:30:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:30:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:30:16 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:30:19 GMT
ADD file:980aeef211cdc1dc441eea6aa6e600765d2ad909294a70a9dfc54b86b8acb82c in / 
# Sun, 30 Nov 2025 03:30:19 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a3b546ef13e5307a10c1657c5a408cce9d7fd8da967afbb8383018e2b2c2a8ed`  
		Last Modified: Tue, 02 Dec 2025 21:29:59 GMT  
		Size: 33.3 MB (33301426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67396e94407424cf9bf12089c47b3de0191e9811df778f7c7d577a0ce4e2d3fa`  
		Last Modified: Tue, 02 Dec 2025 22:11:49 GMT  
		Size: 19.0 MB (18963975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcefd35480496c60d20e52391d3cc2b8e99b310df00d219ea34f600f9ab8573a`  
		Last Modified: Tue, 02 Dec 2025 23:11:21 GMT  
		Size: 47.7 MB (47730732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:52721b62b1bc944ccd485c58ae8f3d1ffa88ef4c8ec958e59d8d8fd57f9e3dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5766506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60b11fb94b47cfe5e3e5302545ffa4694856e6eff38536f128faceacfd008724`

```dockerfile
```

-	Layers:
	-	`sha256:f9f4b233b5e9667a35c04385c3c7be7ce19769956ef681e760ffcddc8d99f26d`  
		Last Modified: Wed, 03 Dec 2025 02:20:33 GMT  
		Size: 5.8 MB (5759146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fefb41ed2016cf457e4ef81fe412ec5b205814ac1c9526a3dbf22ef4eda64aad`  
		Last Modified: Wed, 03 Dec 2025 02:20:34 GMT  
		Size: 7.4 KB (7360 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:dcf175c59a9a865532c75a6d9720cd09004fd93efed5ea08c9cb7c99ae2382ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.1 MB (114127015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfb87c662864e0abeb1489decdcf1d5136b9043401b1e5c230a22a15695ed5b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:28:00 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:28:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:28:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:28:00 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:28:04 GMT
ADD file:9dc48ed376a5f94217dece483aa159c1e9252d86454df2922631eb0d8e28f33f in / 
# Mon, 03 Nov 2025 16:28:04 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:02:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 08:03:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8a7d2071217601e99b42fdc9fbf0f11b498ca9a077822716cc8b2c60912ef80`  
		Last Modified: Thu, 13 Nov 2025 23:04:03 GMT  
		Size: 39.7 MB (39663384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136f99d9e4921d1d5ec73699767f26acccc59c2f03cb3c2902fd8897e7af4545`  
		Last Modified: Fri, 14 Nov 2025 02:03:05 GMT  
		Size: 20.8 MB (20787622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca1c166775b82d33750156d6c084bfa5ea195c09bca4014f1aa368ef94e5c8e`  
		Last Modified: Fri, 14 Nov 2025 08:04:26 GMT  
		Size: 53.7 MB (53676009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:aaacd44a9d21b5b562559d33b4f7b14e6ff2d9ef78bf1e4ff550effc3ac29c96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5768140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fced6af9591e8f91498048713c4aaf7ddbc7c10cbc754b001f1f4b290d180668`

```dockerfile
```

-	Layers:
	-	`sha256:98c70c7ea466093e9eb633b5a3ac59706bc42325286d78c9ad4c0c06984be9d0`  
		Last Modified: Fri, 14 Nov 2025 08:19:57 GMT  
		Size: 5.8 MB (5760827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3490c76075ad187492817ec812f1518cec5337b353a92953bdeb77632535b094`  
		Last Modified: Fri, 14 Nov 2025 08:19:55 GMT  
		Size: 7.3 KB (7313 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:resolute-scm` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:38903f929259f1597ef30e449ae18d0b3bc04f9339b5e7ac8112ba2deb88c7b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102234050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ddd93e3a79821e9569e13262702ba45aaf0c9b6499db39a6f5a813b230e3d43`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sun, 30 Nov 2025 03:41:55 GMT
ARG RELEASE
# Sun, 30 Nov 2025 03:41:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 30 Nov 2025 03:41:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sun, 30 Nov 2025 03:41:55 GMT
LABEL org.opencontainers.image.version=26.04
# Sun, 30 Nov 2025 03:41:57 GMT
ADD file:f463f77192f170ee64673f5278f91bdada45dc922d8fd7d4131d154fe01a4fec in / 
# Sun, 30 Nov 2025 03:41:57 GMT
CMD ["/bin/bash"]
# Tue, 02 Dec 2025 22:11:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 02 Dec 2025 23:10:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:cf3c1d5ff4ce09e68a22f9e6e4bbc83188de5c366e0945d8cc5e8dc699355c91`  
		Last Modified: Tue, 02 Dec 2025 21:28:26 GMT  
		Size: 33.4 MB (33395368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31df4f0b4855de3fe403ca5d6b658f6b8866dffa556bc1fe856875a56977e649`  
		Last Modified: Tue, 02 Dec 2025 22:12:00 GMT  
		Size: 19.9 MB (19867529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13c1b2aaafeb245c9cf5096ea5239ce001ce8766f974bd2ace2c71a24ffa0cb`  
		Last Modified: Tue, 02 Dec 2025 23:11:34 GMT  
		Size: 49.0 MB (48971153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:06650c1d5cbcadd9204af014022bcb8796a00d36786a59dae8d9c538c6cb1c28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5761578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add60505ffff5ae563a3d73f2ac415a2fb9b52446cd378204a604bca5eb06197`

```dockerfile
```

-	Layers:
	-	`sha256:bdd2e872491b942f332ee13e3cd7efc3b56cb732e9cff9cab63be49f62668653`  
		Last Modified: Wed, 03 Dec 2025 02:20:44 GMT  
		Size: 5.8 MB (5754297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4d4859723d6330c9f4cd3ddb50b77eac241ec1ed3ca44d68d2366adb8200fd4`  
		Last Modified: Wed, 03 Dec 2025 02:20:45 GMT  
		Size: 7.3 KB (7281 bytes)  
		MIME: application/vnd.in-toto+json
