## `sapmachine:lts-jdk-headless-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:6005c7faaa461b0a741fa9eac188c3b2af15918c3660de1c5560fb966ab909c8
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
$ docker pull sapmachine@sha256:68ea284a3433e91853615b0b156ce85af3d6bb7028692dc3d4776a7935f6e2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261558624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d6da7ca06c60c2387a56508bbba9a468bdb3ee9581496530e615610af9f93`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6699db415bcda72c8312636c79835162780dc13caddcfd5f7625e167d4adc768`  
		Last Modified: Thu, 02 Oct 2025 14:48:57 GMT  
		Size: 232.0 MB (232021806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c259a731bed191c3de85336fdc3aab4ef4f878f7c34551bf6a89ab303940d0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d87837b2c1f70b13fe26fb4cf6d1d7531d05f89bfa8453511e98922bc85d32b`

```dockerfile
```

-	Layers:
	-	`sha256:759ff2cefed7cce042538349bad0b38bb52dfaf50b462d46a99ef09490210774`  
		Last Modified: Thu, 02 Oct 2025 09:12:21 GMT  
		Size: 2.4 MB (2369684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df23e6f9595195b87cf221b750e39b4a6473f5d07eba19b6567085c00186ea78`  
		Last Modified: Thu, 02 Oct 2025 09:12:22 GMT  
		Size: 9.6 KB (9591 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; arm64 variant v8

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
		Last Modified: Sun, 05 Oct 2025 03:56:30 GMT  
		Size: 229.8 MB (229779775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

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

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - linux; ppc64le

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

### `sapmachine:lts-jdk-headless-ubuntu-22.04` - unknown; unknown

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
