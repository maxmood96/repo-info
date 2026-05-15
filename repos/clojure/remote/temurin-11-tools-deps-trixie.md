## `clojure:temurin-11-tools-deps-trixie`

```console
$ docker pull clojure@sha256:858ab28526286dd7f5a64296c33875dc47bd4e43141023949ae5ff23810f7629
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

### `clojure:temurin-11-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:b8da1f2124730d499b1cba31381930382307842129fc95241364decc19b6ec63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280793216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f93cd7fa4050a4711c16700e927b25640a3f4960e0af26a1cb3328575d8659`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:31 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:31 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:47 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3293ff1d2d491a135e7d381885043acb06bebb1867cbead2fd96eda5ad2f4518`  
		Last Modified: Thu, 14 May 2026 23:35:09 GMT  
		Size: 145.9 MB (145886263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907769ce41625135456b7900c013c77048ac344abbcbf86574bbffc851e554d7`  
		Last Modified: Thu, 14 May 2026 23:35:08 GMT  
		Size: 85.6 MB (85603986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7485cb3021c0b509da9871adf9def9d1e699764ddaece643e043db82407fc8dc`  
		Last Modified: Thu, 14 May 2026 23:35:05 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d316a004a365250673b92d005ceb0347f8fabc2369c5bd9787c635c30a32a139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7505237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fffa3c681344abda17e516a97175a1720cb655df481c41f5b8d29f6ed3d7a33`

```dockerfile
```

-	Layers:
	-	`sha256:c71c055af8bf775f591c4428893cc38de5f52c6b3187e4b2479f43100ccef1a2`  
		Last Modified: Thu, 14 May 2026 23:35:05 GMT  
		Size: 7.5 MB (7490898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4096188a02092270faf9adecdea08ad8281b30872c4b256801341d4e0a8bf76a`  
		Last Modified: Thu, 14 May 2026 23:35:04 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:05c96a3138521f08105d63e948bdbd675837e74bd04cb03027f6c178e4774a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277667307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9752daec35f6e654634c347d1a66b0327f4cf5ce390171add325866d215b6552`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:34:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:34:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:34:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:34:22 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:34:22 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:34:40 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:34:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:34:40 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd214f11ec8d2d9524e2a329c27d869bee3a49f7387cd81c35066c03a66bfdbe`  
		Last Modified: Thu, 14 May 2026 23:35:04 GMT  
		Size: 142.6 MB (142582230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16b39d19edcb487074bceebcba05f52c8c27195620838f896876f867e27d2dd3`  
		Last Modified: Thu, 14 May 2026 23:35:03 GMT  
		Size: 85.4 MB (85414984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d59a65cb365378dc4d79ccc047eb64a726925438cd2505cdde6be3554f41e8`  
		Last Modified: Thu, 14 May 2026 23:35:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d3a3f08be638b0b254ca961726f6aee572f01038655432ee5ed8a7b759f5d1da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b7a91b063f845dab2f0a1dc9ae74cc220118aaf0136bdc2c3288b5f1f6aebee`

```dockerfile
```

-	Layers:
	-	`sha256:080648f1c647c30e892e00ec257cce0dd063f9f7015b127fb3d97c26a13cbf03`  
		Last Modified: Thu, 14 May 2026 23:35:00 GMT  
		Size: 7.5 MB (7498546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676029293f5fc619b27f9b902b05f365afb603f0a4f7df9c6e70cdf6b97cfbc1`  
		Last Modified: Thu, 14 May 2026 23:35:00 GMT  
		Size: 14.5 KB (14457 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:77d733497dbe68a01d9430c2ce9b39a6eaefc91a9db7791b977f6e9567689a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.2 MB (277242285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44608f0b6208c4077af698a5315e8b2b64e80005b3f57175b3731483e289be57`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:26:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:26:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:26:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:26:20 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Sat, 09 May 2026 02:26:20 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:40:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:40:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:40:59 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6819a6f95dd2e4192ab6b7dae90a40976321dcde2fda4665eb71bbac73d5122`  
		Last Modified: Sat, 09 May 2026 02:27:27 GMT  
		Size: 133.1 MB (133110167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e2d5dae79d5f53a209d1b611eb593b1e8c04a2fcf8adf604386b247e2acc68`  
		Last Modified: Thu, 14 May 2026 23:41:39 GMT  
		Size: 91.0 MB (91008306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01bc61d2c47f5807eec08bf42cd3b9e66646af456a214f6e1980baba1f85cd86`  
		Last Modified: Thu, 14 May 2026 23:41:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:cb0a716a0faa4a486fca228fb5a9eaa5c1236b4e8750eaaf3fdb841d0e9097d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7508136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3fd159dca40b16213e32527f068607a556e9e34657eb06b1587f69037b85dc`

```dockerfile
```

-	Layers:
	-	`sha256:73fff1b3d75ace0024fc5b5dd73c68910b1a32405a97b83063ad7dbb0b56f111`  
		Last Modified: Thu, 14 May 2026 23:41:37 GMT  
		Size: 7.5 MB (7494704 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f257d6693f85ebd51506276509fe8aa4dc49261a2928621b6e53e590ea8aa5`  
		Last Modified: Thu, 14 May 2026 23:41:36 GMT  
		Size: 13.4 KB (13432 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:a22382b4897edbf2d1a5ae26e7bedae0fa76809fa0c9364cdc8127ec1c95379c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262590579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:408472164d36634d81de073e669919bf490989b69403926f45d696c56200c71c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:33:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:33:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:33:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:33:33 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:33:33 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:33:55 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:33:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:33:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:49f5adf9d898afa33e019e0f5f9be5e639ceaf0c068ac396b0e56deed0761246`  
		Last Modified: Fri, 08 May 2026 18:29:56 GMT  
		Size: 49.4 MB (49372304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03bb9cf477f64476d69eecca75a6cb3121d4c9e7c850c95bc7fa54e986e7ff5`  
		Last Modified: Thu, 14 May 2026 23:34:27 GMT  
		Size: 126.7 MB (126651735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaaf1071ca844655e76ea2d2e2c66472926ae3f5f996dfeff520934bc0705515`  
		Last Modified: Thu, 14 May 2026 23:34:25 GMT  
		Size: 86.6 MB (86565895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ca1e838f1deac2007368248781eaf3809d50200758c85a634fb944bacbdef1`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6f5efadf90c00ceb4cd4510c4ec63bddf43d6787701091444713bb650a0dca38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7501163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e75286df3be41bff6e29312be7e009b964c2bb6463473dc950b53254fda68a`

```dockerfile
```

-	Layers:
	-	`sha256:29d2eab2564ab606ce6bfcb40f8279abd70f44c7618ebdc74707710f1c2209f4`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 7.5 MB (7486824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a6a60d7c6626a30d88266c0ceb6974cc46865da522bc952b569117d19c983df`  
		Last Modified: Thu, 14 May 2026 23:34:23 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
