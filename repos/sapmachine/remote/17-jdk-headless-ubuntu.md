## `sapmachine:17-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:bb2a18a8fa100bd9a64f644e0ec627f5cd822ffabf9ae6280f2a7f0f76c1b51f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:395859b67ee75add6ccb5d91d60dae6911cf8825e49e623efb078e697e90378c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.6 MB (230560874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c9ca51cc32555cfae6fcf598ebe8b02e133dce75b3e9637bb2c102ce7e2540`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:49:15 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:49:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:49:15 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:49:17 GMT
ADD file:8ce1caf246e7c778bca84c516d02fd4e83766bb2c530a0fffa8a351b560a2728 in / 
# Fri, 10 Apr 2026 06:49:18 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:05:33 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:05:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:05:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b40150c1c2717d324cdb17278c8efdfa4dfcd2ffe083e976f0bcedf31115f081`  
		Last Modified: Fri, 10 Apr 2026 09:34:17 GMT  
		Size: 29.7 MB (29732978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4c07afaa22c984d9acf825fa78197e3c9618de7e4c55798a32c8961a35a037e`  
		Last Modified: Tue, 21 Apr 2026 23:05:55 GMT  
		Size: 200.8 MB (200827896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5290d2615ca8cbcc221e133b780b0d09d4004a7e7f004f4125c1ef2dbe2dcf4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eeda1fba489df1d5e8ce93a4cb3f0a20af91f9bc32ab71a09a7645259c8a243`

```dockerfile
```

-	Layers:
	-	`sha256:1de24fffa9aeb9f67b0e49deb727dba572cf6e9a741fde93f692cfd65580877b`  
		Last Modified: Tue, 21 Apr 2026 23:05:50 GMT  
		Size: 2.4 MB (2357781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4662753c3a4896fc8a2d3c40cd0d8bd302ddccc370409ed9e7261269d20884`  
		Last Modified: Tue, 21 Apr 2026 23:05:50 GMT  
		Size: 10.2 KB (10234 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:7cc177e6ee481198db681a88eaf4f0e658b66e11f475329711990d9293131291
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228444800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732e02176ae82d8395b4e48ff66aec3554e87603771e47ea7379f976d3c71cfd`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:56:52 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:56:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:56:52 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:56:54 GMT
ADD file:c98b7645109cdf61ab97492b90629581b1b7cb925b9d58a5787a4aaeb719f2be in / 
# Fri, 10 Apr 2026 06:56:54 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:06:49 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:06:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:06:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:818154cda96df8bbb276b4f4339124da55756620a1037af15570bc95312850fa`  
		Last Modified: Fri, 10 Apr 2026 09:34:24 GMT  
		Size: 28.9 MB (28875785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52270870d23bdfd793dd42093bb308d71a0fa321df72aef58490a9ce954df90`  
		Last Modified: Tue, 21 Apr 2026 23:07:12 GMT  
		Size: 199.6 MB (199569015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:eb3767fe0f2db8dd55a7b8edb7cdcdca38c50a7c5f1d3d9e074035484c31e67b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2368674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0852e7a16e3ae049e9ca4292a3bfd8ab254fcd9046ed9c6c43bcaf60e32ed3d2`

```dockerfile
```

-	Layers:
	-	`sha256:e3e6dee7adffe75bf3ec0cc38fd15ca2af0e041f6830f45375f95911edc19d6e`  
		Last Modified: Tue, 21 Apr 2026 23:07:08 GMT  
		Size: 2.4 MB (2358288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fcf3996a677879b0cec0db26bb58061154324e8f8865f661407e7635710070f`  
		Last Modified: Tue, 21 Apr 2026 23:07:08 GMT  
		Size: 10.4 KB (10386 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:11d3a4c9b14d7a34c802082f0fb4145085aff94ba9b883d6b680c6cbc2562fc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235866389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67a5764161f8bda9dc039d5840702dca7ea366ff586389165632d0b1a41080c`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 10 Apr 2026 06:58:39 GMT
ARG RELEASE
# Fri, 10 Apr 2026 06:58:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 10 Apr 2026 06:58:39 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 10 Apr 2026 06:58:42 GMT
ADD file:6c2e3684306335751e9b4f6c791c789b8a34813a48130b98adb259dbddc23bfb in / 
# Fri, 10 Apr 2026 06:58:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Apr 2026 23:32:30 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-17-jdk-headless=17.0.19 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Apr 2026 23:32:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 21 Apr 2026 23:32:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9b9e74108592a4e6bb74cdb3f96d255d3bfd39193b9030da034ebfc871cd90ea`  
		Last Modified: Fri, 10 Apr 2026 09:34:38 GMT  
		Size: 34.3 MB (34314178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0d6fd9cdfa189915bc66c18582a7985880cb90c860db985ee6f557221485ce`  
		Last Modified: Tue, 21 Apr 2026 23:33:24 GMT  
		Size: 201.6 MB (201552211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:514a7ee6154bf510b5fa0eb05dd8bbd5d508448e54811794c09ebd07c9da51eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2365554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890d288016d2293885a53e4969d0c14a62ac75e02c33e28284ea267925620bb2`

```dockerfile
```

-	Layers:
	-	`sha256:9874aabecebb1f3df7358a14b037463f7da67389c42e82d786330cddceaf3038`  
		Last Modified: Tue, 21 Apr 2026 23:33:20 GMT  
		Size: 2.4 MB (2355252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f095020e194e7daf495ee1098d7ccbc930a05dace2c695ed7895f75f2d0c3a`  
		Last Modified: Tue, 21 Apr 2026 23:33:19 GMT  
		Size: 10.3 KB (10302 bytes)  
		MIME: application/vnd.in-toto+json
