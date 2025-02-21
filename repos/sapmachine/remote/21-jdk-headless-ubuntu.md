## `sapmachine:21-jdk-headless-ubuntu`

```console
$ docker pull sapmachine@sha256:04e9a54777ec46f1cc98aaee2cc490c93b66a51f545de8373d7089936e8e96b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jdk-headless-ubuntu` - linux; amd64

```console
$ docker pull sapmachine@sha256:cdf787e52a7634f252d2f03cf98de422c6ad87da82db14a105b293b3cd8bf2f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243602935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d45e7c15a2b3ef74cdb93362dfb85fbec82448bffbec1c913e1072afd0617e5`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:00 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:00 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:03 GMT
ADD file:6df775300d76441aa33f31b22c1afce8dfe35c8ffbc14ef27c27009235b12a95 in / 
# Mon, 27 Jan 2025 04:14:03 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5a7813e071bfadf18aaa6ca8318be4824a9b6297b3240f2cc84c1db6f4113040`  
		Last Modified: Mon, 27 Jan 2025 05:09:50 GMT  
		Size: 29.8 MB (29754290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c0157bec2de52d1543fa1fc0bb84119c74eeef8a76dac975b2d1c95421765e`  
		Last Modified: Tue, 04 Feb 2025 04:49:07 GMT  
		Size: 213.8 MB (213848645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:84b237ae7fb5658115e8a96a8c504416737d715b28a048319bf4d5fd94906b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01effec80356d39eac933761ab8440d5ea1c8ca2cbd5e82eeb93704b27434ab6`

```dockerfile
```

-	Layers:
	-	`sha256:9acfeac1af7d4bffd9b616d198875bb282fb126d4774d9dbdbb318a04f91de69`  
		Last Modified: Tue, 04 Feb 2025 04:49:04 GMT  
		Size: 2.2 MB (2236724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4280713dc4873e7e1fe15396803e5fda0655ffc224337c9ee32c78db7ac64d2a`  
		Last Modified: Tue, 04 Feb 2025 04:49:04 GMT  
		Size: 10.7 KB (10652 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:3ded598c61760659202f57ab11fa1a83ba2f791c501a535d5aefcd48329cce23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (240977875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c26f2a88d584f1c846678877bf7d5a81fb42534155d353cfd09054be1c65c248`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:14:51 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:14:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:14:51 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:14:54 GMT
ADD file:68158f1ff76fd4de9f92666ad22571e6cd11df166255c2814a135773fdd6acd7 in / 
# Mon, 27 Jan 2025 04:14:54 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5b17151e9710ed47471b3928b05325fa4832121a395b9647b7e50d3993e17ce0`  
		Last Modified: Mon, 27 Jan 2025 05:09:56 GMT  
		Size: 28.9 MB (28893598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621a88737c16f03783de88ca059f9f04b240545a0dd45b5b4fb646217d140a07`  
		Last Modified: Tue, 04 Feb 2025 15:26:54 GMT  
		Size: 212.1 MB (212084277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1e789f8a78ce5e9ffe74b3f6dcb2d0a4038295e93982f3dd89cad6c20e9f86ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2248059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43abbcebe1c5d51fddda80c09b95daeb691867469630742be76910f300e8ff99`

```dockerfile
```

-	Layers:
	-	`sha256:3b6a0efb4593e3d61361f7ddf091a30902783be95db3e915ce9fab189eea9b0a`  
		Last Modified: Tue, 04 Feb 2025 15:26:49 GMT  
		Size: 2.2 MB (2237243 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:992c1a78b5581239dc6db96f04365153d816264092020e269513b63680b183e0`  
		Last Modified: Tue, 04 Feb 2025 15:26:49 GMT  
		Size: 10.8 KB (10816 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jdk-headless-ubuntu` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:72c6f1faa505df3d56d28c35be176cd4ccce585f4d9a6821ef347ca2e0e4a9d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.5 MB (249458178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda018ac32e21b7a2083300320489a024c12c25e9472c7e9d1a6a9bc03726b12`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 27 Jan 2025 04:16:03 GMT
ARG RELEASE
# Mon, 27 Jan 2025 04:16:03 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 27 Jan 2025 04:16:03 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 27 Jan 2025 04:16:07 GMT
ADD file:8c71b040cc97f9d076a34d57cd957e6b33cdfb8f115e1ba283b674e6aad793d8 in / 
# Mon, 27 Jan 2025 04:16:07 GMT
CMD ["/bin/bash"]
# Mon, 27 Jan 2025 13:39:13 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jdk-headless=21.0.6 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 27 Jan 2025 13:39:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Mon, 27 Jan 2025 13:39:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63bb950362326716a27cf0240223ca9b5b5528e2922804f1973429bcc74e3262`  
		Last Modified: Mon, 27 Jan 2025 05:10:08 GMT  
		Size: 34.4 MB (34389824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b45668982c2cecb1e0d24096835d8086a05f13bc0f9232fe2fc5d87291307b`  
		Last Modified: Tue, 04 Feb 2025 14:36:06 GMT  
		Size: 215.1 MB (215068354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jdk-headless-ubuntu` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1388cf3ce86a14a23330eb5015d9b12af04cf194142334285709d6b77a918cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2249410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:923b83e0be6f7568f6d4bd8286d36f0a1f0409cdd365d4a9b3063b0c8c460824`

```dockerfile
```

-	Layers:
	-	`sha256:7fd22f36c7054c186356a8dfb0e527d04e7eaf86a5f4b5e051d9803ae6ec4456`  
		Last Modified: Tue, 04 Feb 2025 14:36:01 GMT  
		Size: 2.2 MB (2238684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f68c0d8a460d51025c48016b992c9a652dd1da5f2b439cbeecc1d927a639391`  
		Last Modified: Tue, 04 Feb 2025 14:36:00 GMT  
		Size: 10.7 KB (10726 bytes)  
		MIME: application/vnd.in-toto+json
