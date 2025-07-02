## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:5886d66fa2faac382d79aeb09c463f06558d70323f42768481705578c05abdca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:72b3138ceda42944a75393b0592a37f279d1d707319c9790ad33852fddf5b9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.0 MB (243049871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27ae092ddca5b8378dfa3be7e3d14a3addd6a3c41364966fdadc94c451595cc`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:36d136943d44dbe1fed342b933d9abb8e0694bf141a0c0af85ca83cc73e25158 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e735f3a6b70199ad991c5715d965a4d858540eca2be18be0d889698e5a0a3e8c`  
		Last Modified: Fri, 20 Jun 2025 12:50:42 GMT  
		Size: 29.5 MB (29535686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51d68f32678384596edd501742ea54356dc11fa37501d2e3815c76319fe3dce`  
		Last Modified: Wed, 02 Jul 2025 03:13:09 GMT  
		Size: 213.5 MB (213514185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:5c4f7b4a4c14c8acce131560e74e31f23abd9ecd6253e705fdfa01429fbf4bf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b2e93658fc9a38f16210301dacaacf1c895ad7efe04f348354d544a820ca3e`

```dockerfile
```

-	Layers:
	-	`sha256:c80a3e8a122995299ce32453e6f7d037f63a897c60db985466a2d85cea3f665a`  
		Last Modified: Wed, 02 Jul 2025 06:07:29 GMT  
		Size: 2.4 MB (2378318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015d6f3eeb3fc6cf5881e8a0c3f3354d6daf85e447419228c1772d1cd0080bc2`  
		Last Modified: Wed, 02 Jul 2025 06:07:29 GMT  
		Size: 9.6 KB (9628 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:f614c49c48672a62808b14766b982a5a1589ce224fe8cf2997b3b1a774ccda49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.1 MB (239079218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b336db2f637b4f38375291d73a516df00ff4dba99818e017d19548548e8b1f1`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:420f880e94b721d5d51db26959a0be413bb646cea8a083b48bc7ac884c7fd405 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e730d307d74e767a94e2a36b22cfa82c38738f86f671c4fc0e3c90dadb75afbf`  
		Last Modified: Sat, 21 Jun 2025 02:35:16 GMT  
		Size: 27.4 MB (27359272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedcfbfca18d00509a400f7b3fc65dac765595402f9687e829b7bb2a221a0c81`  
		Last Modified: Wed, 02 Jul 2025 06:42:36 GMT  
		Size: 211.7 MB (211719946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:3ebf48b4b81aa19f532fa88bbc69eb30b043cd1ad6991d4cdd56c4f55a0e2cf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a41de34582d9c6c929f9056f9a2e92169c9fb4c703b163843ecdf07d30b2cf`

```dockerfile
```

-	Layers:
	-	`sha256:f16e7b2c3df52fd973211be86bac63e92c6c886cf683c97f59162e340b77fb79`  
		Last Modified: Wed, 02 Jul 2025 09:06:30 GMT  
		Size: 2.4 MB (2378014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0594f017e033c11c17b8fca23847871d5921b5b083a4e893962ed1873930811`  
		Last Modified: Wed, 02 Jul 2025 09:06:31 GMT  
		Size: 9.8 KB (9756 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:44011a0a39af8936a7d0970a7cf697028bf3dbe125e019aad171fffcc75a7403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.1 MB (249069755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaacb5983ffdba72091844ea5c37d1586237a3b86dd8b626673faa994733d36`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:37 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:37 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:37 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 16 Apr 2025 10:34:37 GMT
ADD file:5a3eca55a1307e0619bbe09c4beb95f2ca516da79fd68c8aee17cf1b99d1e6d3 in / 
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:37 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.7 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Apr 2025 10:34:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:596d3daf42a32d1b87496f9f15c5f6b6e3760f136eaa5e4351b4c6a439599d6d`  
		Last Modified: Wed, 02 Jul 2025 01:20:19 GMT  
		Size: 34.4 MB (34442621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93540c09c077c01422ef79d58f8b93d3e085b0e8ce872ebf22401ef2f41622e`  
		Last Modified: Wed, 02 Jul 2025 04:54:38 GMT  
		Size: 214.6 MB (214627134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ca936c165bffff6511dac51df5ca7d761ca850dbbb58fe621dd8e75a36f8892a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2390109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b4f0f11d7c8b0bb4412e18014aa11db98fbb91b1eac6973446dbaf342f43a9`

```dockerfile
```

-	Layers:
	-	`sha256:d9b6cb4a70a678b30fc5e0d763a9531cb78c0a9c4bc179e75d1f6e63a7788d66`  
		Last Modified: Wed, 02 Jul 2025 06:07:38 GMT  
		Size: 2.4 MB (2380425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbf2fa42896dade86234dd3786ef79d306c51f1c764f7e398425980fa100fb90`  
		Last Modified: Wed, 02 Jul 2025 06:07:39 GMT  
		Size: 9.7 KB (9684 bytes)  
		MIME: application/vnd.in-toto+json
