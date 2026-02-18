## `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim`

```console
$ docker pull clojure@sha256:042920f1923ea6eea0b6b7a05d547a7ab3d5b1b7aa86acf672f89d01a3a3f166
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b5bb388bad10cf6aaa0c995908a1d007f48040b7c17b9584497cd19c411cd399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243713284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245f7f7b60e33cc4b89bb060c38cb01327726a11cea7d6e2a9835cc58ede6881`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:42:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:42:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:42:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:42:05 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:42:05 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e552471b02e027bcee22b0619465eeae54ccd5b839a7ff78d233827180e39298`  
		Last Modified: Tue, 17 Feb 2026 21:42:44 GMT  
		Size: 145.8 MB (145806756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce45ae7522419938b90205f199fd31b8a3c6e64e419ae47cf360399c75152eed`  
		Last Modified: Tue, 17 Feb 2026 21:42:42 GMT  
		Size: 69.7 MB (69677394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee6fbe3b0a3a2b769460a119a619d1ee4f7555fb46e4564212a7045a86e0beb`  
		Last Modified: Tue, 17 Feb 2026 21:42:39 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:605f19a87485a523c9b1b5d501fb74a50b80a1c37abbbad3b77e8ebf06931159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f4b0466f2ebba799184513826ce771fadaa41fddf1a986fa310738c10395905`

```dockerfile
```

-	Layers:
	-	`sha256:a8f27170ac70dcb9367f345f6ff55f2f0f4dd6a6e019635147ed8a8b20670372`  
		Last Modified: Tue, 17 Feb 2026 21:42:40 GMT  
		Size: 5.1 MB (5134795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d2cfc94e79be3d0c8f5a7b55713063d3c9f7700626eae5507e925740417f30b`  
		Last Modified: Tue, 17 Feb 2026 21:42:40 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f50d0e20d1f1e421e2ec91a353515c07f746c4591eb6095b633695ac8a6cd444
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240282530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4a388f0082751cc0470212d286c6e8816c676e6a4869bcceda04a5ab13ac4d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 21:41:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 21:41:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 21:41:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 21:41:49 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 21:41:49 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 21:42:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 21:42:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 21:42:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba50e41a69da0d7f4ad6afd275d25c1f1db7db01e731125cc0f3653aaac274f`  
		Last Modified: Tue, 17 Feb 2026 21:42:27 GMT  
		Size: 142.5 MB (142501431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb0c16b6d1f18945e9e527ff4a2b66863ae3c51283fd7c82be875d3d1dab5570`  
		Last Modified: Tue, 17 Feb 2026 21:42:26 GMT  
		Size: 69.7 MB (69672629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad032da276f6d7d23e7821bfcb1791442d4d4bdfb791ca99332932e0524baa0`  
		Last Modified: Tue, 17 Feb 2026 21:42:23 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b5dca92dc5904f5b7542304d5ed223742a63b9599dc9b4f806934e4cb958b18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f24be742990302a6ba6fb7c3033a304cfb10f764ab175b5d06751e6bee1ed2`

```dockerfile
```

-	Layers:
	-	`sha256:37c1f9b2d8c02d86357e3d83556b98478943aa4dc07972c277077ca4d8d49ec7`  
		Last Modified: Tue, 17 Feb 2026 21:42:24 GMT  
		Size: 5.1 MB (5141174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aea850f98ac335e9d8230c5c79a3c11c5bb478a9fb1f2ce770f43ff73e73e589`  
		Last Modified: Tue, 17 Feb 2026 21:42:23 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:7f12712e3bd710271a7ddf06af0a360626128d3a837ea41c77467c5ec2ee7119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240581385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31688233065e30a61b70e84d9bf94c80bd48f8ef872fffd308943e3aa137d163`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:33:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:33:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:33:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:33:16 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:33:19 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:39:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:39:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:39:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b47947f163eae116857a151bacee4e62eeef47f193f3d24c01851afc3df70f9`  
		Last Modified: Tue, 17 Feb 2026 23:34:52 GMT  
		Size: 133.0 MB (132997795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79c068226afca5c4eed66c523d7606c5a38ed4f15c58e0fb6c33314cdec7f76`  
		Last Modified: Tue, 17 Feb 2026 23:40:46 GMT  
		Size: 75.5 MB (75514231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc675e5641cbfd8b74e9bf6b68f1593a4b3febeefc55e37df8d38f6156391f4`  
		Last Modified: Tue, 17 Feb 2026 23:40:44 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:78586615aad33997d9ccf3d5a55299912ec8cae0fcd090a8a324d04ac5efa059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5153653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ed6c150941da404fadca50630cc2201acfd379ab5abe3c8bccd0519190d092`

```dockerfile
```

-	Layers:
	-	`sha256:5a8c11c6202d587bb4e998e926fbd7f8ab757ec29502a873ebb7edbbb3ffe2d2`  
		Last Modified: Tue, 17 Feb 2026 23:40:44 GMT  
		Size: 5.1 MB (5139338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:342d927106a20a403cc804bd2a083800e297e246f7b598c3673a650d35266758`  
		Last Modified: Tue, 17 Feb 2026 23:40:44 GMT  
		Size: 14.3 KB (14315 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b4e341bf44518cedc68220c6d8cf2d31b073a111714f063eeb05f05e7a444ddb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.9 MB (221937238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93f496d127f9889d668905a3ec123123f9f9fa78150118eef90564dce12c233d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:03:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:03:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:03:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:03:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:03:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:03:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:03:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:03:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218d4292c40642aab1eab8c514b6dea5a53435c0300c56d394484419091018db`  
		Last Modified: Tue, 17 Feb 2026 22:04:13 GMT  
		Size: 126.6 MB (126562060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed138bf8a5e0a0c831e19df446bc9df54f5d8c6bdd3a3fbdd64794851cb18b2`  
		Last Modified: Tue, 17 Feb 2026 22:04:12 GMT  
		Size: 68.5 MB (68490150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5816dac5183464010a5f3c783b1a10f490cae823b41c11fec18011eba497458`  
		Last Modified: Tue, 17 Feb 2026 22:04:10 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1602-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a0ba6cd64fd00752bed69adea0bd751b6690a5c45f0505157a79035901b6d866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4191a7169f390be4f21408fb57ccdbd1b31a82fdc919ec9e0255b49f56e20b`

```dockerfile
```

-	Layers:
	-	`sha256:83d84aabf5b88c6d4ad57cbd1344d91a589c8271cfb5098306a17b5dc0e0bf6e`  
		Last Modified: Tue, 17 Feb 2026 22:04:10 GMT  
		Size: 5.1 MB (5126120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b141ec77dbb177d58d2e80d25fd8913ea7056c00ed3ee62b8d5579d175b4d8b`  
		Last Modified: Tue, 17 Feb 2026 22:04:10 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json
