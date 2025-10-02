## `sapmachine:lts-jdk-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b4088019533cabd8dce8ed03bb08f8f6f1f4dce0377b6acfa69907d518b6f10c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:a63fa9623f5a5c5efbdc36f84071f508f92198820597325ef567296d01e9caee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261558840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86c18219ca1f2c61c4d23c574b85af740b546766f8daf99c93dd07be6138a224`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 19 Aug 2025 17:17:08 GMT
ARG RELEASE
# Tue, 19 Aug 2025 17:17:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 19 Aug 2025 17:17:08 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 19 Aug 2025 17:17:10 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Tue, 19 Aug 2025 17:17:10 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338d831fb60ac6f44984b62cf0bfa75f203a69ab68c41a21d1782da6556bb69c`  
		Last Modified: Wed, 17 Sep 2025 22:10:09 GMT  
		Size: 232.0 MB (232021905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8197ee6dfb3e1c72139ae84e5a72914645ee22cb6d29250bdfd97fbb34fe5203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2884f4eeaa7d9a247989b97600a445977a851ea461abf43d9c6e1fe9a408c9f`

```dockerfile
```

-	Layers:
	-	`sha256:bfdf2a24430694aa55c61db5ff5bc526a4d09f569a724cd8348ce2ebbb04581f`  
		Last Modified: Wed, 17 Sep 2025 21:10:51 GMT  
		Size: 2.4 MB (2369684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f033d882eb0179ccfc3be91d960cfe346ca861528b27af6147953e568096f874`  
		Last Modified: Wed, 17 Sep 2025 21:10:52 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:a1269dcc6d0671a9a7c644bc433951484339098b0cd6bafc7b5e626c7d5a62d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.2 MB (257162882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33cc761c18fe009f2320edd1971f2d09ad24229bde17def467a76577417bee79`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:7a71c1d52054f8e04c815eaec639d14adaaa62346860f4003201834430b7ff18 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f85691aa4b9092cbb48212c835b78068e3321656ba2c306dae491e1a02d1b4d3`  
		Last Modified: Wed, 01 Oct 2025 14:17:05 GMT  
		Size: 27.4 MB (27383107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7054aa6a7b5b07b18962b7995dda16f4904d979d6e080e4b56c9648b0f7c6c`  
		Last Modified: Thu, 02 Oct 2025 01:34:02 GMT  
		Size: 229.8 MB (229779775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:65c4824ad9794557b890859f24d8c37f7ebe6c32b693e145334119d287182d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1847ff9731462549d12f4a79500c5e018244dca78fc14895cc37fb467743db1`

```dockerfile
```

-	Layers:
	-	`sha256:9e281253ea4940299c643deb85a841211eb05a9dc0434ba2479b736bfbeb8552`  
		Last Modified: Thu, 02 Oct 2025 03:10:21 GMT  
		Size: 2.4 MB (2369377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380b065f0424971b2e44e7498ea3513f365e2c56056a4c98dda160ae6f6d8363`  
		Last Modified: Thu, 02 Oct 2025 03:10:22 GMT  
		Size: 9.7 KB (9720 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:49bd05d19f85427ff926fc7c3d31eb3c2485c9f3a2f2ceb7ae219bcbb960fa6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.0 MB (267048869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28367e70db2c690246a2a47b088e6fe3383192766eaf07e7f1ca1f50aac18fa`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 17 Sep 2025 04:28:56 GMT
ARG RELEASE
# Wed, 17 Sep 2025 04:28:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 17 Sep 2025 04:28:56 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 17 Sep 2025 04:28:56 GMT
ADD file:0aa9da71877b87fa24e5611ae918040b9e86da1da320091962f21431bce21835 in / 
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 04:28:56 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-25-jdk-headless=25 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 17 Sep 2025 04:28:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-25
# Wed, 17 Sep 2025 04:28:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2fbe0139d4362c4f9e73d9ece05926b347d08fa0942b6a7a53617f13f42d1f91`  
		Last Modified: Thu, 02 Oct 2025 00:24:59 GMT  
		Size: 34.4 MB (34446789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5dee4bbffa328f123ff60197d983f3393fa186131ccefdfc35fa28f3829b007`  
		Last Modified: Thu, 02 Oct 2025 04:21:45 GMT  
		Size: 232.6 MB (232602080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:474b352634ffe8c786fbbf0fd3123af9a365d981b9a5e7f1388bbe96f1327742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7356d9ec7ccb6612534a18bc37aace1ef5973e09f931c55e7fe335caa6535a8d`

```dockerfile
```

-	Layers:
	-	`sha256:9c955717a40865817bd0fd2847afa5cc68b8d5a8f0e317eefd30a5ad3b1a0158`  
		Last Modified: Thu, 02 Oct 2025 06:10:34 GMT  
		Size: 2.4 MB (2365157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7984f374e310de16ce3357dda5ea77ced718a7005e4e7e2b9c10fa12b3a79702`  
		Last Modified: Thu, 02 Oct 2025 06:10:35 GMT  
		Size: 9.6 KB (9648 bytes)  
		MIME: application/vnd.in-toto+json
