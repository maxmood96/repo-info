## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:3cdcc840c36d7b4020a9f0761f41bba946078d5afd0588f4c46774b223becfb3
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

### `clojure:temurin-11-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e6922b60e5591b287879da3f18f84a48a0aa7b47ac1ab746e462ad7a140ef7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.7 MB (246734577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b41183d5561186d34705abc60be0be0517afe4a1369ff7375b113868d1574c7`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:51:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:51:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:51:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:51:02 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:51:02 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:51:19 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:51:19 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:51:19 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:27 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2d701df7c32711b465549c3ffcdc7967b1e1625b3f50335c0f171206a20804`  
		Last Modified: Fri, 16 Jan 2026 01:51:44 GMT  
		Size: 145.0 MB (144966605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e333b6d86640629ae6f716b602333baefd185aeebcf41aa11c2c40241b021a1d`  
		Last Modified: Fri, 16 Jan 2026 01:51:42 GMT  
		Size: 72.0 MB (71993642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3c60ed0c81ae2209eb24b5aefb03f865591e622f36edffd12b81b22df1ccf71`  
		Last Modified: Fri, 16 Jan 2026 01:51:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3109f1f7ae3753d9a8598a7df7d429a33c1fa4be9f53186fed6340bb9b11861e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f8218d4b94033e91621a941e5268a04a366b343345e19af578aafa5e69b8ef`

```dockerfile
```

-	Layers:
	-	`sha256:1c4f05e4c874e5f4dd7594eaa8251fb99fd8b6f64c9087205c69428699e839bd`  
		Last Modified: Fri, 16 Jan 2026 01:51:40 GMT  
		Size: 5.3 MB (5276436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae82228e5b0693960a2c78fd6f00adce5d2f3440614f098c0dbedc7d89dae3b`  
		Last Modified: Fri, 16 Jan 2026 01:51:39 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d200ccf4ba2a9cdb0ebc882c31290ba8f16a3817799cba8924f49d5aad923aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243670906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844696af1acc8f65f43377ade67ccc5e3af9a98d6f0d60d44a7391343f060c65`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 01:55:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:55:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:55:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:55:04 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:55:04 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:55:21 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:55:21 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:55:21 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87dc663a8bfdbd12d47861f3d8977e963dc866fb77ec1ed2b31f19cbea4db647`  
		Last Modified: Fri, 16 Jan 2026 01:55:43 GMT  
		Size: 141.7 MB (141729881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65e3dd4a75253d68b7bc88c37bcf58483249165b629d5f47773605ca93f57da`  
		Last Modified: Fri, 16 Jan 2026 01:55:42 GMT  
		Size: 71.8 MB (71806339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74c57989864117f1e21a976be633342fc9edce3a7730ffae1fac6ad46543be5`  
		Last Modified: Fri, 16 Jan 2026 01:55:39 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1eb5d53b1831edf3c8e8c0a5fb1756cc360e445aac18e8e7251d8c3e56b8fac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab488160daeaf23f653f6f05d4a71e5d9e0e9e4db53e8ad07cc6b0ca12354508`

```dockerfile
```

-	Layers:
	-	`sha256:ca5b35785bb66bd187645728fc0a9061474e11cdcb51464d02789f932faf5c0f`  
		Last Modified: Fri, 16 Jan 2026 01:55:39 GMT  
		Size: 5.3 MB (5282823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2efde20d9bbedb47aeed9155e5173219d1e5ebdbeed09b7321369e5259c009ea`  
		Last Modified: Fri, 16 Jan 2026 01:55:39 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:b0356b1124a8bf7d8e028521a4d00d6d78e6e6d321ad8a485c9ca872abb226a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.1 MB (243067292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3301842779944a82b95e4cca6206208b8414441dae53dfc479a8edffd7aa95c`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Fri, 16 Jan 2026 03:01:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 03:01:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 03:01:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 03:01:56 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 03:01:58 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 03:10:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 03:10:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 03:10:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:06 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535e69c188d843a40931640c882aeab8cb565638d03ecacffc478c1a783da983`  
		Last Modified: Fri, 16 Jan 2026 03:03:52 GMT  
		Size: 132.1 MB (132079785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ea7c1018746e5923ccd3e60574b8cbc1cb6c98cbaa41020f1a0b3e15331262`  
		Last Modified: Fri, 16 Jan 2026 03:11:28 GMT  
		Size: 77.4 MB (77391262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d78f347a105f58e893ed27ad4efb3799f12708d14747dd6a8d80fe016b503404`  
		Last Modified: Fri, 16 Jan 2026 03:11:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:91704236b20116173f3e51d1960bc6edd2bdaf94e073fc509e9bf6d25fc9dcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab24461d6b7ec816a6a555e576b7f96b4b41e242cf238d70d792faba41d173b`

```dockerfile
```

-	Layers:
	-	`sha256:a255d0c4e6ae8d5b0cfc57e978e0422ec966f24ac4fc563f9127f72587deb992`  
		Last Modified: Fri, 16 Jan 2026 03:11:19 GMT  
		Size: 5.3 MB (5280192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2076e3ad96d9f6a51d89329747a704ebdd84d3d991ed8167d2577c15ce86200d`  
		Last Modified: Fri, 16 Jan 2026 03:11:18 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:331613c40adcbc51531c13d836efe6046d79de2a61ff57c817b7d447ebf28992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.5 MB (228480957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a109b2581ed4b59354081ea20a664e79fce607f84966eee0132c73525ce7d07`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Thu, 15 Jan 2026 23:11:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 15 Jan 2026 23:11:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 15 Jan 2026 23:11:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jan 2026 23:11:24 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 15 Jan 2026 23:11:24 GMT
WORKDIR /tmp
# Thu, 15 Jan 2026 23:13:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 15 Jan 2026 23:13:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 15 Jan 2026 23:13:28 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:27 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d189c892ac739b1461897667cb3f0702a6090d4dd1b8acc3ad2f6d38d27b1f26`  
		Last Modified: Thu, 15 Jan 2026 23:12:01 GMT  
		Size: 125.7 MB (125694841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9932a15c2905406433716d1e89e7dc123df15ccb5d3513cfacffd4e70d1481`  
		Last Modified: Thu, 15 Jan 2026 23:13:51 GMT  
		Size: 73.0 MB (72952061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:952e96f622a57ec0aaa5e583c421fb48f9008d726f7dba3c75c13abbc03d1236`  
		Last Modified: Thu, 15 Jan 2026 23:13:49 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:5b061d5e162beeba044f82a0f9339025f8433b0581862212bef16f10862ec3df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2636788f37ff3a071379c80cab1925aefbdcbf893d01d7609fbda336a913fcb9`

```dockerfile
```

-	Layers:
	-	`sha256:82971837ed9df3307d82372eecfa2a4546962566d2165a4b73a6a0692dfa25f5`  
		Last Modified: Thu, 15 Jan 2026 23:13:49 GMT  
		Size: 5.3 MB (5272364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e0349139eae4361354ee4decb53a110e7ed3beba4d5ddb1d1790a2ee1422928`  
		Last Modified: Thu, 15 Jan 2026 23:13:49 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
