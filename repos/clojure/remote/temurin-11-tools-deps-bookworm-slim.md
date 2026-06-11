## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:e63b662b5fff89b0718e8d8298f69dfd9b5ed6d37c9c3d330085cf36878deeff
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
$ docker pull clojure@sha256:2c2553754077344ecb6f9ecfc518994e47616f680721cde9cd42d16eb986b35c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240767215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfe39668283b9cb81f14e0c4b438755b6a95a533128eb8c2624e6c7d173e54a0`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:17:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:17:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:17:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:17:55 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:18:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:18:08 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:18:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8415ea36450529e872537283a8d6acd46d7b633138b8522d11c7f8fa07132f9d`  
		Last Modified: Thu, 11 Jun 2026 01:18:29 GMT  
		Size: 145.9 MB (145886202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11e3ce77f8f79163f5c418b9828516c57f435978ba473fa127466b45c3301d4f`  
		Last Modified: Thu, 11 Jun 2026 01:18:28 GMT  
		Size: 66.6 MB (66642745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c314d8bbb6c53af7637e852486fb7f3aa95b60c01dc52288480820f54546409`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b83fda349c6db822d4b4fdec44436700070be48ad89ec0fb856af495cb535263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5147936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfa54a5530cda200c9a05e98e577156159640325214b46b12d8403a783ae30c7`

```dockerfile
```

-	Layers:
	-	`sha256:af6adcfed2c38e932b79ecae1a1540c8640f8cd2098862b5bfa131c6f35f063b`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 5.1 MB (5133515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb3df191e8cfc0aa2aa90d7ee84460c7eed0613934cc57716ee91ae57fa3add4`  
		Last Modified: Thu, 11 Jun 2026 01:18:25 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aa92aa3d92e89d044221452ff1d99d7c9b92645a489cab5f53dd4e42deda4b4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237348383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ca6c901c757ed95988f115833004fef0cf83cc8d8dc35c8ea15c65d22fa4c1`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:21:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:55 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:56 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:22:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:22:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:22:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245303d6ed9e6619ebd4ad5485aa2b12a85a7dd8b2f5c7cfb6a780b6392241bd`  
		Last Modified: Thu, 11 Jun 2026 01:22:33 GMT  
		Size: 142.6 MB (142582228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3915e8e3d83a549de2fb515af4cc84bef0d0c62b83056e4b535481e09ec3d5`  
		Last Modified: Thu, 11 Jun 2026 01:22:30 GMT  
		Size: 66.6 MB (66643204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4394f7b5b41af511c96d7e0818de54c9dd4b8984c01729583c81961c5211d5b1`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2869a43a375be3c2cf285487105c1c25afb736fda54978882ce7cacc9c529f2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5154433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ea20a16becab1e65f67e12508bd18f98a8d512de1290dc298181f0d965f473`

```dockerfile
```

-	Layers:
	-	`sha256:57592bc408b82d8666cefa046b30edd21cfcb41ec235cd4c307ee291dc30b827`  
		Last Modified: Thu, 11 Jun 2026 01:22:28 GMT  
		Size: 5.1 MB (5139894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80de22f1da825eb9405da5579e7d521f10abf1deef02eb1606ce2e03da447f0a`  
		Last Modified: Thu, 11 Jun 2026 01:22:27 GMT  
		Size: 14.5 KB (14539 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5e13332232c38e0b7a4d22762d942eba854c38bc62ffbe6de7b68f14f812092f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237662295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:851e6cfb30024bbc12841d690c32356f6bc4e3640128579be252eff4952f5cfe`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Thu, 04 Jun 2026 17:47:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:47:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:47:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:47:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:47:50 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:48:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:48:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:48:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c0d285f6de64db1a5978e6b8056ebad15a1c14c41574df90fd2cc4d026505`  
		Last Modified: Thu, 04 Jun 2026 17:49:12 GMT  
		Size: 133.1 MB (133110217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:948177c9cc2f84801073612b513cfcd37999f61e5954a8f37e0c768dd4c8de68`  
		Last Modified: Thu, 04 Jun 2026 17:49:11 GMT  
		Size: 72.5 MB (72475692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cdd9d791b302b4eb56bfc52d94451fffa4e5a592ca133397742308379276a0b`  
		Last Modified: Thu, 04 Jun 2026 17:49:08 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ab8bdf46d07b55f2d21a66f751a153bc4038a439bfb07f64de3017989e77f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5152509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d60b9dae90beb33131526b43a8744dff823273953938bd739e46c2895d00c7e`

```dockerfile
```

-	Layers:
	-	`sha256:35c20607c3b0eeaa11032246ef45f2ede305956d5bed805982a0637773b1cf04`  
		Last Modified: Thu, 04 Jun 2026 17:49:08 GMT  
		Size: 5.1 MB (5138040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45e08bc34eee9cef85c05affbcd8a62a64ffe572b32ced4b2669e94a7da6408f`  
		Last Modified: Thu, 04 Jun 2026 17:49:08 GMT  
		Size: 14.5 KB (14469 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:46d836d6cdc3e39f9d35fcf24c5a8c5444e102c63d8a3270b2118acca021c95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.0 MB (218997821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde27c4d9b9afc96d329e7f989ec75102b824e73c711deb1da97ed74c4a7f553`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:07:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:07:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:07:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:07:44 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:07:44 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:07:58 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:07:58 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:07:58 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6483bebe0f30256cfdd9c6f96373508f6b33d18b4bc61668ee641c700aa3108a`  
		Last Modified: Wed, 10 Jun 2026 23:41:10 GMT  
		Size: 26.9 MB (26893508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dda81ad80e015ec42415cf3a2240538b016afbb15a1bb6475b226ea9d596656`  
		Last Modified: Thu, 11 Jun 2026 03:08:29 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf3a15aaa0ed1cab63cf69cac6a49afc3729c3cf6253e2911fd4b20c88f690c`  
		Last Modified: Thu, 11 Jun 2026 03:08:27 GMT  
		Size: 65.5 MB (65451932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbb5dbcb30c64a8969d0de3a12a55695a1fc1eca7800a1e7a78dc653e3b2263`  
		Last Modified: Thu, 11 Jun 2026 03:08:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1e0fdc64a23ed9145e98e3a75ea28ef75c0287711c20367a46c88053ee7b76cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:453abdcbd86f43bdd1938a16ea2249854812f87f55769f463ab2a11ea4e9123f`

```dockerfile
```

-	Layers:
	-	`sha256:b90a39435d643c8af4053281379d51585a943d6f4d2ed8863be438dc25cfe5ba`  
		Last Modified: Thu, 11 Jun 2026 03:08:25 GMT  
		Size: 5.1 MB (5124840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4a020a1f02f03712101a9f464c20b9d46c42f4d6d9ebbce73d1f41fa9a85ee4`  
		Last Modified: Thu, 11 Jun 2026 03:08:25 GMT  
		Size: 14.4 KB (14421 bytes)  
		MIME: application/vnd.in-toto+json
