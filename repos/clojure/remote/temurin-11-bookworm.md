## `clojure:temurin-11-bookworm`

```console
$ docker pull clojure@sha256:1e2e6d4798f7cc169dd29c3b393e944e3a9ee3e7b3771df28732240546cff8d0
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

### `clojure:temurin-11-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9fd30453739d781dad1c4bdbcb3365550f300533ee0e72d0fa976f1564b90da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.6 MB (274594124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f344def6f07b29d56f2022efc50d6aa3fb9cd0f7f6de2663097253d6664ac1`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:51:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:51:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:51:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:51:33 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:51:33 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:51:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:51:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:51:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c8443a297fa42e27cb10653777dd5a53f82a65fbc8b2d33f82b8722199f941d3`  
		Last Modified: Mon, 08 Dec 2025 22:16:25 GMT  
		Size: 48.5 MB (48480736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868f42113aec77f60e1ab76859aeb124f8d0a1077d150190dc28a8d4a25b0a08`  
		Last Modified: Mon, 08 Dec 2025 23:52:30 GMT  
		Size: 145.0 MB (144966651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56355359dba0d926a53672411c1f858939ee8bb1e27152371f003423ef0d8e12`  
		Last Modified: Mon, 08 Dec 2025 23:52:31 GMT  
		Size: 81.1 MB (81146097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b21e40662e0a7fbb06f7f9821de426623b89b0c3133a259ec611fbc059f8d67`  
		Last Modified: Mon, 08 Dec 2025 23:52:22 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:575b1398f7a7efa51e7a1741067519a203b38ca78ff9658eaf0cf2fa949b7358
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7409240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fd41c5bf71f92c4a91d6f76239789ef2e1be06dddaa4a5b7d660dce0954b65`

```dockerfile
```

-	Layers:
	-	`sha256:38e8211aeb5a443d3ad5c3b5e17bd33ab54726bfc85dbb7cb088fe88d0176c32`  
		Last Modified: Tue, 09 Dec 2025 04:36:07 GMT  
		Size: 7.4 MB (7395031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a47d8601033f9bc1e0ef44b9a08fd96b18ca656120f945d1b2a57fde71abea7f`  
		Last Modified: Tue, 09 Dec 2025 04:36:08 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a56438c97d3fa8a2a4c673a667a0f0219609507ef210184edf717f14f28e8000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.1 MB (271122031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a63b662ef55eb1cdd4f7ccc7f027ca64c84bca9dbd58f710d260e07fa575485`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 23:59:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:59:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:59:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:59:05 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:59:06 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:59:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:59:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:59:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7f2b9668af76f73927725e2d1fb5d7224604d8c4c42cb8cdecb502257d9101c4`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.4 MB (48359071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bc02dff71540038e71531425ebf2b8713de0996ad9acaecdeae676fbb9db44`  
		Last Modified: Thu, 11 Dec 2025 12:56:51 GMT  
		Size: 141.7 MB (141731552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e246338c4ee723b44b2af7c5f3302fe00a5167fd74211852c3bc25bf8904dc`  
		Last Modified: Mon, 08 Dec 2025 23:59:57 GMT  
		Size: 81.0 MB (81030765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cf079338e4f5eecc6f611a2b782c6822ccb15136d66d4686275ab6a9a38746`  
		Last Modified: Mon, 08 Dec 2025 23:59:51 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2fc0daa29c9209b81714683ec55425901342fa5fde0dff82d3222420527906a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7415739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3d9c668578fc4f1ff6447aec89267eb7f6dd71ed2818f5c9dfb53c108e5aa9`

```dockerfile
```

-	Layers:
	-	`sha256:1769fd89c3c0395d8f223962c4fbf54279ea2efc1d09ee31ebdd75d0d066c475`  
		Last Modified: Tue, 09 Dec 2025 04:36:15 GMT  
		Size: 7.4 MB (7401412 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccfeb252ad13fc839de84a95c191e7571e6ccb88b1aa26d597c96b66af7c55a4`  
		Last Modified: Tue, 09 Dec 2025 04:36:16 GMT  
		Size: 14.3 KB (14327 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:ca44c543a48142e449f721f4cd35c6768fbbb6d7bf4d90278ee9e448c603bf8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.4 MB (271395603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edc98d35110c6bb9ebdb95fe09ce7f1189a8b49f6d5e43ce1631f752a694e1c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Mon, 08 Dec 2025 22:40:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 22:40:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 22:40:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 22:40:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 22:40:17 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 22:42:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 22:42:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 22:42:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c088128ea77bb5c706bb00930020ea2fba147060275f49c5a7be6b54af5ca7c8`  
		Last Modified: Mon, 08 Dec 2025 22:17:06 GMT  
		Size: 52.3 MB (52326977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea2fdeb54b2cee4553e719a73e258ac39eb559f4d51f9bcd020d029ca3c9cb5`  
		Last Modified: Mon, 08 Dec 2025 22:41:54 GMT  
		Size: 132.1 MB (132081948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd355991e7385444e5cafd469580ecf35781e4aec07b75e6fd8ece5d9f98c5fa`  
		Last Modified: Mon, 08 Dec 2025 22:43:34 GMT  
		Size: 87.0 MB (86986034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f4e41cbc994bb1354f754f03c379d7d93dd4e7d1e080cb8b8bebace6de7ed7`  
		Last Modified: Mon, 08 Dec 2025 22:43:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4d9f6058244aa0e9fdbd94459deb0596cb78b0e1f4575353490ce3c21dc69c23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be24b265f685ba5d9d66e5326b5c844ac626c171ca3c5e9465f895d7b0ed9a85`

```dockerfile
```

-	Layers:
	-	`sha256:183549a8d5788b9337a3674f2368479ce819aa2f6fbe9e2a9628993fa07f9461`  
		Last Modified: Tue, 09 Dec 2025 01:35:25 GMT  
		Size: 7.4 MB (7399630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642503cf0bf6d98ca5bbb6a1af5a88f7f09802f1b1e135c2426bfb8e905a4a99`  
		Last Modified: Tue, 09 Dec 2025 01:35:26 GMT  
		Size: 14.3 KB (14257 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:19a52a8dcf719482b0d281fced0e3b4dd9f87b22b9aed882b48c39b4ebf75744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.8 MB (252789386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224d2a5bdfe92cd96327bce225fc325ddcf9140ec8d474f4cfaaccbe8c94d622`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 01:26:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 01:26:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 01:26:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 01:26:04 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 09 Dec 2025 01:26:04 GMT
WORKDIR /tmp
# Tue, 09 Dec 2025 01:27:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 09 Dec 2025 01:27:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 09 Dec 2025 01:27:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f1896ba83f603ad81e0d8cb48b496e763b4b781a68efe11f1b6de9da929514ea`  
		Last Modified: Mon, 08 Dec 2025 22:15:09 GMT  
		Size: 47.1 MB (47137665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0da402ac0335fa8c106407457a6e9dff3b61dd890c09a3107b689a3f9fc23b`  
		Last Modified: Tue, 09 Dec 2025 01:26:58 GMT  
		Size: 125.7 MB (125694469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f82488b75f09aa3979fc551135a8c357981700477ada70fc67ef46482637f7`  
		Last Modified: Tue, 09 Dec 2025 01:28:05 GMT  
		Size: 80.0 MB (79956608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66aab979bb136f1b7698bf56449c3173deacf8824b5e724fb90eb6331fb76c2f`  
		Last Modified: Tue, 09 Dec 2025 01:28:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2a717e94a7a50c8c63edcc2fe236ef31362096ae25d320b95e7bed950c113971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ded4bb3ea350261f589a4fa64b11700e156b8a835c15c9cd037ef07653ca6652`

```dockerfile
```

-	Layers:
	-	`sha256:cd77bc0c8a7b6b35992201218c42bde4741d243386081088c4508e8c09f652f5`  
		Last Modified: Tue, 09 Dec 2025 04:36:26 GMT  
		Size: 7.4 MB (7386354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10dbfca9a913894ddba832a3976862359c782cc9af4772daefbb3f52f558e52`  
		Last Modified: Tue, 09 Dec 2025 04:36:27 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
