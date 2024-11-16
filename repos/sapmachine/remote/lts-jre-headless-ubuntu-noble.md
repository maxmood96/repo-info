## `sapmachine:lts-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:6ec8c83ab5a38f7719395d4c1b0015c57997ad1dea9a0da1d879bd4c498fe599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:3b221677a4937f2be2625c4089c8727bb480d4a1bda5403c418829c1fc1c71aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88608991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83034fcbe755c2d5ee11b4ef9028264c344c3c7912fda65942d07b04e46c734`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:54 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:55 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:57 GMT
ADD file:a3272496fda5a8d021b94dccaa6baa685ded51e9d23edb05f0b30978a83c9fc2 in / 
# Wed, 16 Oct 2024 09:25:57 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:afad30e59d72d5c8df4023014c983e457f21818971775c4224163595ec20b69f`  
		Last Modified: Wed, 16 Oct 2024 12:48:06 GMT  
		Size: 29.8 MB (29751784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec031a40c7c5dde6ac44a0f72896ef14d370156b1a665472cdb8ff6060af3e5`  
		Last Modified: Sat, 16 Nov 2024 02:57:16 GMT  
		Size: 58.9 MB (58857207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:fda7094034c34d8a2fb6b9b5231fcac5e48dd6097c23e7923742845db4f01337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cfad10b29bd6a8d3583a7942d14109aa4cad803beb753098abe0b9b5c0f59b`

```dockerfile
```

-	Layers:
	-	`sha256:0bc242df718b87b62c5c988fd0ffac95dd4f925df36d9b49bd27add1c1be18b6`  
		Last Modified: Sat, 16 Nov 2024 02:57:16 GMT  
		Size: 2.2 MB (2150031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb52b6cc932a0a2342d29d997554decc47086b44b848a02196fac1a5f418dfa`  
		Last Modified: Sat, 16 Nov 2024 02:57:16 GMT  
		Size: 10.7 KB (10651 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:4826f75946dd5790affb53d2785aa069afcb111089b95aa10cb12328a948e208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86902247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b86bf0f055eb1e5d3abbaeeaebd7236fb20736ad771c71a43e34ab6bf5fd3e5c`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:25:38 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:25:38 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:25:38 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:25:40 GMT
ADD file:f45100f0b1cac298fb43b06ffef22e36a90991ee414d6dd825694bbea3365d40 in / 
# Wed, 16 Oct 2024 09:25:40 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e3366dd687552c0533285c7066bb8e937a5aaa2ff3a0c1c7f1305b3310399895`  
		Last Modified: Wed, 16 Oct 2024 12:48:12 GMT  
		Size: 28.9 MB (28892425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae88fb2ec0d31ae52535dfef4d6a6130fac5978c3cee1c99c1f78979bb5def2`  
		Last Modified: Sat, 16 Nov 2024 03:49:58 GMT  
		Size: 58.0 MB (58009822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:845f5a8cdabe2453a3dcdb78b6e483d30799a540275842f23cf52f3718735448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2161364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1729136b40c00a6d588ca5766109f5bd388a4b893728661269be99bb2bc7b98e`

```dockerfile
```

-	Layers:
	-	`sha256:2e42ac90731683fca49727454bd783699a9e8faaa9d21c1de892817ef15c9dbf`  
		Last Modified: Sat, 16 Nov 2024 03:49:57 GMT  
		Size: 2.2 MB (2150549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1186e91c5ac6e1bfd9b3b27024e42d94d60618ae19a1f109540ffcffbab8917`  
		Last Modified: Sat, 16 Nov 2024 03:49:57 GMT  
		Size: 10.8 KB (10815 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:1b2456fcca3c31f1e4dcabbbe17909da0f5515fba105df812eb8a3da6db5cecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94753706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14412fa8e731970cd438818493b70c7323e529648afa4c4cf18c1d31fd5caa02`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Oct 2024 09:26:09 GMT
ARG RELEASE
# Wed, 16 Oct 2024 09:26:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Oct 2024 09:26:09 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Oct 2024 09:26:12 GMT
ADD file:8427b57c40c05cd946f6695dbd1754b0a521a98decd2cdc16eeb114c7128804a in / 
# Wed, 16 Oct 2024 09:26:12 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 12:49:09 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.5     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Oct 2024 12:49:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 16 Oct 2024 12:49:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:991986948126e836a79c1084e3bee33549a43b83cabfe16234aef5b4b30d86f9`  
		Last Modified: Wed, 16 Oct 2024 12:48:24 GMT  
		Size: 34.4 MB (34388822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9212d6e47848ba9aa61328d805dd0a9ee28c1999f85c8b0821903236ac46a312`  
		Last Modified: Sat, 16 Nov 2024 03:50:12 GMT  
		Size: 60.4 MB (60364884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:0317f4b41aa9556a8d75f0bb4c32d4ffbbefaea0864d57c57dee5f12952b51af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d78b905b307f44e9c861b37252493a9f7f37c22a90e912f571fe9ed29e3b7b8`

```dockerfile
```

-	Layers:
	-	`sha256:9d0f502d6a3cbebc05d16f87bb3fbe71cb061da15d8e21c76af510a8cce74434`  
		Last Modified: Sat, 16 Nov 2024 03:50:10 GMT  
		Size: 2.2 MB (2153935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024b8f3b548ba1c7a6f8880b1a0fc0c88eee3056062dc24863568809aa3e0804`  
		Last Modified: Sat, 16 Nov 2024 03:50:10 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json
