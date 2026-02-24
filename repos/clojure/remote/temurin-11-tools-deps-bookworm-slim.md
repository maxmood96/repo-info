## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:40cb2e9976c44069b39649f2e5c305ff7b57ad902b0aa04c621c17f71347a017
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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:30e5bf2b312619a406d0dd958399f4f172cdd9d33a1653e38d09f283d6546594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243721536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97ee2dd2acf201a2f0ca9f95c9b8ac613045fca93d46fe9e375deba00196a66`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:53:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:53:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:53:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:53:54 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:53:55 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:54:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:54:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:54:11 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac9b998bbc7e0e221cbaa3131bdd5cc21fc9e066238fea5f6ad9c1f5bd83081`  
		Last Modified: Tue, 24 Feb 2026 19:54:32 GMT  
		Size: 145.8 MB (145806748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a285a8704d294701a783c3e1b5bef876b77078bf4512e0439f6c60c6c5ac5fc2`  
		Last Modified: Tue, 24 Feb 2026 19:54:31 GMT  
		Size: 69.7 MB (69677865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1949e0abe39c547ce85083f76d0044ca5ec3b35a23803044afeb5bca41a9cc`  
		Last Modified: Tue, 24 Feb 2026 19:54:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ceebdf136cb422d13f0444fb287e285aad4ce730f505efde9fdb8961f048e2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5149062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8b0b97cf8472bed0ff9a4148ee0ffc755b13cca8b9a4073646788b20566bc6`

```dockerfile
```

-	Layers:
	-	`sha256:4fce8408a4309d89f2fc3c3aaefe8fae418764f321c31bb3f76f26b91712bb18`  
		Last Modified: Tue, 24 Feb 2026 19:54:29 GMT  
		Size: 5.1 MB (5134795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54a47a10cfb61b160db1d566ef9625fb1f27be64e32e986565e3a1d538e2f176`  
		Last Modified: Tue, 24 Feb 2026 19:54:28 GMT  
		Size: 14.3 KB (14267 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9dd27af98f35a85ec91a81722caa2d487d43ac57464dcd7c74b4611804374e26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240290925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ca665d09ee056a2b952add3d392bc2cbce9c017c683242335761d1c1300a339`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:04:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:04:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:04:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:04:48 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:04:48 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5871f4fbe7dfcc9a36025e9899c39bea7d61c0cbee0950ee344fc1ad5ecb34e`  
		Last Modified: Tue, 24 Feb 2026 20:05:26 GMT  
		Size: 142.5 MB (142501445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff47636a43c4fb63663963bac7994cef190c77e04ced38dea31ca7299385e754`  
		Last Modified: Tue, 24 Feb 2026 20:05:24 GMT  
		Size: 69.7 MB (69672757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e6b144d0e3d97eab8459e45306b0951f5e3ee020e5ac0dd1b275941d015a58`  
		Last Modified: Tue, 24 Feb 2026 20:05:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:236fe691ac9d3ea8c4283b32189f964b936d356c35007d06641e4b054a5c6514
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5155559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9372878196320d36304c859e00a4e914a71c7e3bb44db5fe1a17eba57617bba`

```dockerfile
```

-	Layers:
	-	`sha256:f18c6a72f628ddc8bcf6db1e0ca65390a206ef35174af19995cdca07bd52bfb4`  
		Last Modified: Tue, 24 Feb 2026 20:05:22 GMT  
		Size: 5.1 MB (5141174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b09242eca6d5763c458535ac10e72aa610bd909061655d5b7220e5edb03c04e0`  
		Last Modified: Tue, 24 Feb 2026 20:05:21 GMT  
		Size: 14.4 KB (14385 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

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

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

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
