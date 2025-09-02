## `sapmachine:21-jre-headless-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:d7506f91f9873a72409de4c5e7f8007e8aba2a6ee956fe9c881cca66759cbfbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:85df9d4a7ca4564653f2536f3a0e6ce0eb4c6c157af30220f7f2f8a14e9f94fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88738316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e433dee76dbbcad04f7c0d563d737965958b0aa7bf39e9fdef193ccd53d0f33`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:e67907c77897d27192314f6c4fa0112b6f7dce3e127500516535cc50fe736c92 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:76249c7cd50397d2e8c06a75106723d057deaba0ffbc7f4af1bb02bcf71d81cf`  
		Last Modified: Tue, 19 Aug 2025 17:39:10 GMT  
		Size: 29.7 MB (29723064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0423c69a77cc3746b0c9268578dfb7c8ec3db9e7f5feb4bf6b1d0011403dd8`  
		Last Modified: Tue, 02 Sep 2025 05:10:05 GMT  
		Size: 59.0 MB (59015252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:373b7fefd6e2229f74ff6d448c071b2dd84f926587338ee6eb282d338917e7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650f73116564408875cbe353707662e508e04061f8cacc5b4e04a8bc99c8c18`

```dockerfile
```

-	Layers:
	-	`sha256:e2ad6e5e385a0811b6d1735cade28876d3086e0983aea2631ec1f4e7b2e54dd4`  
		Last Modified: Tue, 02 Sep 2025 03:07:48 GMT  
		Size: 2.3 MB (2273850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2db12d4b1351e5d01d62ef871f3c040b320ca1ccbd86b23d5cb74cd65d958de6`  
		Last Modified: Tue, 02 Sep 2025 03:07:48 GMT  
		Size: 11.3 KB (11306 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:92ecf91c7e840f3b77c319ba105d4b627c67e685d53c2b19fa613a360cd07215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87046903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb81552e7a647e192846c0ec0ec6258562db3ba22b67553a34070952bb876d0`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:b7517e9b93ca90114b86d36fa835651ac45b762e188edb92fc804391a8989e04 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cc43ec4c13811c515d52d11a6039f3659696499c8782f5f3f601a3fdedf14082`  
		Last Modified: Tue, 19 Aug 2025 17:59:52 GMT  
		Size: 28.9 MB (28860240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03caf7270bbc82b1c84d7f3900c5f08c5dec4e64c65f67344acab4f34c5eb7e4`  
		Last Modified: Tue, 02 Sep 2025 03:08:11 GMT  
		Size: 58.2 MB (58186663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:7ab15a1c0703500510b313624a91e4985ace1aae6c2f1b59305126965875a8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2285888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920af522044d7424cae42750802770d0f8dcd1b3cab2f55e96e4d122fbf1c901`

```dockerfile
```

-	Layers:
	-	`sha256:71e4a53e60e9795ef057eee277203398fdb66aaa3ed73f6fb314edfe92cd1d98`  
		Last Modified: Tue, 02 Sep 2025 06:07:01 GMT  
		Size: 2.3 MB (2274393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70af918096a8fe9d3156555fe81603f17ddabf053c81ac21e1c4860c91239b0e`  
		Last Modified: Tue, 02 Sep 2025 06:07:02 GMT  
		Size: 11.5 KB (11495 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-24.04` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:7c2fd57703829ba967f2e7cf46104c801d30a76418243589dc217e2b83990e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94386328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6741fec84e8f9f54b2c7fcaffb969b0945b5dad9a8fb5404ccd9113d305b26dd`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Jul 2025 19:58:06 GMT
ARG RELEASE
# Tue, 15 Jul 2025 19:58:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 15 Jul 2025 19:58:06 GMT
LABEL org.opencontainers.image.version=24.04
# Tue, 15 Jul 2025 19:58:06 GMT
ADD file:55e5af389c76b79c77275691d488810a1fd875fe7e47b4b14a8b70f1230bf1a2 in / 
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["/bin/bash"]
# Tue, 15 Jul 2025 19:58:06 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.8 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 15 Jul 2025 19:58:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 15 Jul 2025 19:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5128fb40eedc06172c4cc2920b45ddb874f5b42c161d0a777ed53f0b9f80b8e7`  
		Last Modified: Tue, 19 Aug 2025 19:17:46 GMT  
		Size: 34.3 MB (34329533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71c07353af9c39eae6b9600e6ad5978283abc4552869129aee812b5df3a4a99`  
		Last Modified: Tue, 02 Sep 2025 02:06:20 GMT  
		Size: 60.1 MB (60056795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f5b635d983026463a3f447e465d9c457ebe8648549a1b9931254b402e4f8641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2283260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0218c1e4abe086173ef93c48918992bdbcab73f9a964a2d49abc7e9139c8f3a0`

```dockerfile
```

-	Layers:
	-	`sha256:d834951e6d4af092ebe710576c671964c7df1918aa193f922eb81d5092a75147`  
		Last Modified: Tue, 02 Sep 2025 03:07:56 GMT  
		Size: 2.3 MB (2271868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a01626735a8c87f3d21bc1872226a190f649bd618ee130f2f498e33aecb236a`  
		Last Modified: Tue, 02 Sep 2025 03:07:56 GMT  
		Size: 11.4 KB (11392 bytes)  
		MIME: application/vnd.in-toto+json
