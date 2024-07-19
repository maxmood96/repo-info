## `sapmachine:11-jre-headless-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:2c368a7602e3ffa5856eef213900475e5676419844ace34bc555e6fb493a0515
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:0d8f38c72831ef53730cc960b23113bedb2e1642d1e17df5eb25a4fdfd027b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.3 MB (78262684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ff1fb2c2ecf985658ba1152883ac241b01ac6b4b8dbd9391d4c30446a9a98d1`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:19 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.24     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 18 Jul 2024 15:16:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e2d77b8981727276a079f34e89bb46fe9c9b9dd82228dfcc200ad8f3b08abd`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 48.7 MB (48728629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:83ebc7325d2536133c441e3b76dae3a5b3b3b21a670fe09dfe8ed1bfb0e08543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b995f91b60a5850e43c7d475c299cfdc0d3518c21776d18dde220699957df7`

```dockerfile
```

-	Layers:
	-	`sha256:19463c26c96d3b4a5fbf99c76e4dd1891945050a449d872780026221b44cd02b`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 2.2 MB (2156982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d016e0e0c932058d72b71143df98a7b9b72c94ab3e2869506f69ee522e5016a9`  
		Last Modified: Fri, 19 Jul 2024 18:00:13 GMT  
		Size: 8.7 KB (8678 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ce149a475d09623b95196040d8d7bd24a13281874787b69f7bb91bb8c1e03eab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75364787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58257dcea5891695d4b82d7bd10fdbdebb5d85895c4211ea15c80542c24fcfd0`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4ce000a43472e4a2527834764b5044674760f1e2a766480798d03a93b51a0b39`  
		Last Modified: Thu, 27 Jun 2024 20:18:34 GMT  
		Size: 27.4 MB (27360025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73edb7aea051d1b28af6b2193e5552bc432cb73a2439c950946059bdabbfc745`  
		Last Modified: Wed, 03 Jul 2024 00:08:47 GMT  
		Size: 48.0 MB (48004762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:ff9232b9f823d6790ebf9934821d221ac006265d963e516a0a0faf64342d2a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25fd493f0c2763b970bb0cbd011d79a55c02bd9c177f102f89996a85daf1fbe4`

```dockerfile
```

-	Layers:
	-	`sha256:61fe360cf59bcfef2f411fd94d5894158de0fc1a13d043a5a7a9014fd8d87907`  
		Last Modified: Wed, 03 Jul 2024 00:08:45 GMT  
		Size: 2.1 MB (2132389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f9fa08133895251975a21d2e5447df62057cb5805db6a6a58eb7eb99d0cff89`  
		Last Modified: Wed, 03 Jul 2024 00:08:45 GMT  
		Size: 9.0 KB (8997 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:11-jre-headless-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:dc8daf831dc4b841751f27674ef2b9fc0d6d0d8f9c0aa11248dd642ccd3c19a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81634855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32e3c276796a1b3eb112caa7be0a47c3f110956e04a55318a0dd08124996d600`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 13 May 2024 10:06:56 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:56 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:56 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 May 2024 10:06:56 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Mon, 13 May 2024 10:06:56 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:56 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jre-headless=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 13 May 2024 10:06:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dcb5d217f9f18d3486ceb1894319d66c6f49a84670fbf2ac2f4dd47935357bfc`  
		Last Modified: Thu, 27 Jun 2024 20:18:46 GMT  
		Size: 34.5 MB (34461081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9daeead953df2da5a471eea04d3a2f7c51f7c250723295bd112f7bd890f5506`  
		Last Modified: Tue, 02 Jul 2024 21:41:28 GMT  
		Size: 47.2 MB (47173774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-headless-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:c3aaf149c0846f39b4af11960a75a202abaaaf0dca798fd7d8860b2fda5dc599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2144738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e45e3c3b2524abc25761d6b05d29cf97e52f9eb338ba66cadab5504491a7e8e`

```dockerfile
```

-	Layers:
	-	`sha256:18f85efdca8ff8073947e998419b9b26da274955c1f3cdc98a14036eba349b00`  
		Last Modified: Tue, 02 Jul 2024 21:41:27 GMT  
		Size: 2.1 MB (2136006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad0eb28b7236e3c034294a077b341bbe2e199ec548b6394ad879e86415ed2acb`  
		Last Modified: Tue, 02 Jul 2024 21:41:26 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
