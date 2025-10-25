## `sapmachine:25-jdk-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:16ec0fa2a9e441d58410202b3fbb3f3e931e736966e52d703842b9b2ca72b577
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:747f1bd9d6acf05cda310088042485c60ca3de31ad25f6d3a8aebeb23b65431f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.6 MB (249582036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb4e43fcfb5d538f34532f09e6a7ee0c1e1c0f1aaa8fb0b0a44cc4a2ef562f1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:05:07 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:05:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:05:07 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:05:09 GMT
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
# Wed, 01 Oct 2025 07:05:10 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c0bac6273906b619fdecc972c7463dfb8c4b48b13f66576030142a868c47ea7`  
		Last Modified: Wed, 22 Oct 2025 19:02:41 GMT  
		Size: 220.0 MB (220045218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:23d9515349b1f8a86b9342cf2f81ede730aae1b5a7650989fbcf4c0f052e5f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bbdec9a54ea2ff4231abc32434a8815ba59fb25188fb585cd1d910b52b081f6`

```dockerfile
```

-	Layers:
	-	`sha256:74fea56551845d5adb81b62578dab356300e44c57fdf151e6f1dbc45e1894d71`  
		Last Modified: Wed, 22 Oct 2025 06:13:33 GMT  
		Size: 2.6 MB (2621784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c3317a64362a6e254f6737240c451f28f7a6b33a9744a9e8d2f11746f0daa3d`  
		Last Modified: Wed, 22 Oct 2025 06:13:34 GMT  
		Size: 12.7 KB (12733 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:cc2d878f0f2fbb3d07b8c9be1bb6eff72adf3cfa4300cbebacd40cb4daa03f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.1 MB (245124282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c376e974263988d435d711284f6acee728d19659c7ed0390f25ff5e50d4b4c02`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:16:10 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:16:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:16:10 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:16:12 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 01 Oct 2025 07:16:12 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991d0a7ee2a4887018f1af224e2e0411598022cb0bd8088d85f3407af577afed`  
		Last Modified: Wed, 22 Oct 2025 20:12:16 GMT  
		Size: 217.7 MB (217741175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9ff53a7b145a6003c7a8f2635f1af55274de77ed939c67580d4d034236461a5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ce0ebf34846b5a08f895bb92bac493bf7661d0f8a287e8c1ef5ed1a6e22766`

```dockerfile
```

-	Layers:
	-	`sha256:fec393910709b46e77edf9098c6e8d1b4312913ef5c99fc06fbd5bc78a59c35a`  
		Last Modified: Wed, 22 Oct 2025 03:10:11 GMT  
		Size: 2.6 MB (2621607 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cb17df5595fcb59d2a3a4d20cc100ab2cb2550195450100445316ab51e85327`  
		Last Modified: Wed, 22 Oct 2025 03:10:12 GMT  
		Size: 13.0 KB (12980 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:98c9d2c250a9d2e2d2a3920e8db30885d334424371bcd5a4cf5b12a680ce3773
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.2 MB (255217730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a15877c17fc79ca96bbf04234a3b54adaeb29e14ef1a099fc938ad082bbcef9b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 07:06:37 GMT
ARG RELEASE
# Wed, 01 Oct 2025 07:06:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 07:06:38 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 01 Oct 2025 07:06:42 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 01 Oct 2025 07:06:43 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d472cd026e9abad5acc12e56e3029168e202c5b0d517d5aed47db14651d9e1`  
		Last Modified: Fri, 24 Oct 2025 23:30:57 GMT  
		Size: 220.8 MB (220770941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2a1619d59c0c3a553e9cc8ffb1292781042ae2d0c077bbe88b07268f77f4c8f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2630255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cb434edaabb873d4d8e3f428b28ffa2e9c8882d936e7b9b472945088d91696`

```dockerfile
```

-	Layers:
	-	`sha256:e420dd903803cc962fa1bca51f4e0f6a69a3ac119dfb840d733a7c404be40603`  
		Last Modified: Wed, 22 Oct 2025 15:10:27 GMT  
		Size: 2.6 MB (2617407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:407fc25eb6ce751a76bf32bbe1be407ffbc80a593521aea17044cb426252a7c8`  
		Last Modified: Wed, 22 Oct 2025 15:10:28 GMT  
		Size: 12.8 KB (12848 bytes)  
		MIME: application/vnd.in-toto+json
