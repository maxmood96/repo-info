## `sapmachine:25-jdk-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:2692aa9aec7e51b647f7676dba2cdc8077f756c48eb74847aa00adb080e81337
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:25-jdk-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:2c2e06cca91e44407255e47b6e0e42ad489d1e5a69497d1956cd348cf3dd927e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.2 MB (250154504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554dc7a96a58ca47afe1b6af1ab012fadf47443a9c0a46c8744ed983e3922e4c`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:23:01 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:23:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:23:01 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:23:03 GMT
ADD file:ddf1aa62235de6657123492b19d27d937c25668011b5ebf923a3f019200f8540 in / 
# Thu, 16 Oct 2025 19:23:03 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:37:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:37:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:37:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:20043066d3d5c78b45520c5707319835ac7d1f3d7f0dded0138ea0897d6a3188`  
		Last Modified: Thu, 16 Oct 2025 21:15:22 GMT  
		Size: 29.7 MB (29724688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb65f3b3b66b3d1ba4a9cb176b3bbb9222dd94d1218a0bd018a1b95c406ce6aa`  
		Last Modified: Fri, 14 Nov 2025 01:42:33 GMT  
		Size: 220.4 MB (220429816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:19456f241252aa8a97e7a38a3a603cdc04cd25804f6b099e3764114ae7320ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2616281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3632eb86dbf494defdf6c5943363adef13f7c289e59769d89c0fc333088d40e0`

```dockerfile
```

-	Layers:
	-	`sha256:8ee6f76f64028a68097857ffc7479244e03bedc43ee18ed1a775cc12c46ed84a`  
		Last Modified: Fri, 14 Nov 2025 01:12:23 GMT  
		Size: 2.6 MB (2598925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa8f52ad52f2330b0631afdd89a34deba39f74ba0c76d5b22234d243db8ffa3e`  
		Last Modified: Fri, 14 Nov 2025 01:12:24 GMT  
		Size: 17.4 KB (17356 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:829c35af6d7600fbe5293b931e122895c3e14d9b03323f19673509f5fb0da2ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.0 MB (247048591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:741c1643aa73c071152d0dd4c58cd498cc9fb17cf02d2a0d2ff75065382323cd`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 16 Oct 2025 19:26:52 GMT
ARG RELEASE
# Thu, 16 Oct 2025 19:26:52 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 16 Oct 2025 19:26:52 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 16 Oct 2025 19:26:58 GMT
ADD file:44fdb45bd3a8d9bd9c66b716aa0bb6ee11b6fbcceb59ee0eb54165785a35dfcb in / 
# Thu, 16 Oct 2025 19:26:58 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:36:42 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:36:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Thu, 13 Nov 2025 23:36:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97dd3f0ce510a30a2868ff104e9ff286ffc0ef01284aebe383ea81e85e26a415`  
		Last Modified: Thu, 16 Oct 2025 21:17:48 GMT  
		Size: 28.9 MB (28861957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c6010e2e23970c6d32ac7f316bbae37bc4c141bff6adc9b6d7037a709f7cc4c`  
		Last Modified: Fri, 14 Nov 2025 02:00:00 GMT  
		Size: 218.2 MB (218186634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bc5f7e275b2ec8690e77ce52798784ab1d797d5159f4f9cfa92179cbae0d076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2617498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5175c8d2dcb0bdc9cd6a76019020c4d9b603c34979732341278bf80e6c222f1`

```dockerfile
```

-	Layers:
	-	`sha256:207d8e0a99b2c18e9c930c7d095af69481741a5feeae867fdb2303950ea2aabe`  
		Last Modified: Fri, 14 Nov 2025 01:12:29 GMT  
		Size: 2.6 MB (2599714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb985ae9e8fa7921c940ddff8a2e7cfa63a775f5bd4d777a1d5d49a45452c897`  
		Last Modified: Fri, 14 Nov 2025 01:12:30 GMT  
		Size: 17.8 KB (17784 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:25-jdk-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a782f3b97c82277bf88b564ac855a8dd14bebd9852b6ab1b422e05c7b0dec25e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255562669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c287246335c82228940f0c228563098e0af1cbf9ce8654c13f6ddd28480dcd16`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 01 Oct 2025 13:02:29 GMT
ARG RELEASE
# Wed, 01 Oct 2025 13:02:29 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 01 Oct 2025 13:02:29 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 01 Oct 2025 13:02:33 GMT
ADD file:e06669c9bfb72bbbaf1c25efab4729831236db24361c42e37dbbc7b4eff7a82a in / 
# Wed, 01 Oct 2025 13:02:33 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 21:30:17 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk=25.0.1 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 21 Oct 2025 21:30:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Tue, 21 Oct 2025 21:30:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:199e3830c89a37cc6980743d7c9e0e355251d050c55eb838183c9cf64fac375b`  
		Last Modified: Wed, 01 Oct 2025 17:22:52 GMT  
		Size: 34.3 MB (34303525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2447fd34f2a917b60d1990444663859bc6b67973aeffd76dffd9e967df5f9f5`  
		Last Modified: Thu, 23 Oct 2025 15:09:09 GMT  
		Size: 221.3 MB (221259144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:25-jdk-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:afa6faa505e2beb23d6803e4d27d4362564c1e2938b84506fce6b09707412b04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2612185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaf2ea74c6ceab48a334a23069073c8a294d1d4e38f7ca38e26be9de6ec46e8b`

```dockerfile
```

-	Layers:
	-	`sha256:48e55bf67cc3e1d24d077bb4bfe5037aa3f9ed285f72dd046607106b06c6d4d5`  
		Last Modified: Wed, 22 Oct 2025 15:00:32 GMT  
		Size: 2.6 MB (2594580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14711c65c26c30c4bb345185de633aca49366467487a319a77d5bf025c4fe65`  
		Last Modified: Wed, 22 Oct 2025 15:00:33 GMT  
		Size: 17.6 KB (17605 bytes)  
		MIME: application/vnd.in-toto+json
