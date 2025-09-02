## `clojure:temurin-11-trixie`

```console
$ docker pull clojure@sha256:0f571730b75b799a10a5b4fc1d3015d25b7f21512e1725b5a468421cf49de20d
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

### `clojure:temurin-11-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:568dbbcccf8d097a418da6976f8c6d07bbb65b3454ceea869db6093248b60e52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280470302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f610f1031c3a60579ff4679aff1e48f33399ec41f372ee90fc0d1513d8bbd2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:80b7316254b3093eb3c7ac44bb6c34bde013f27947c1ed8d8afe456b957ebfdb`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 49.3 MB (49278280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3576d5dfba93d945e19d11fe0e9f7b6a236261ee9ea08a6b54ef13ed587ed20`  
		Last Modified: Tue, 02 Sep 2025 00:17:21 GMT  
		Size: 145.7 MB (145658266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d8be6a7b744a0a27c1214e987419760b0ee9f01375eff838a8ea31df3ee6b68`  
		Last Modified: Tue, 02 Sep 2025 00:18:06 GMT  
		Size: 85.5 MB (85533110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f3389595214110348ba054106516fdc0bc0dafbbc831d3c9a51434b5c35f09`  
		Last Modified: Tue, 02 Sep 2025 00:17:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:bc532fe22598a2a75df97cad4d911d638495a1292ee1ef40d675a76e8aa12f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7496590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:744024b101f5ffb8f48f39b51a1b85e0a50a311a46c525dc7e30f9cf327363cf`

```dockerfile
```

-	Layers:
	-	`sha256:a9f27e6a0dc92617b0b64f9e077fe4158adb456ac8e3fa2f09247516c9f76f05`  
		Last Modified: Tue, 02 Sep 2025 03:37:26 GMT  
		Size: 7.5 MB (7482362 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40807405aeb518ff68cebe0323ff8e255548e29bf17d836ec12191f72b9d7d64`  
		Last Modified: Tue, 02 Sep 2025 03:37:27 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd942728c438a512c4bb989151ea3257acbdc65a033f5d68480d476bed60518f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.5 MB (277459391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c699493732cc2a8ef9bc539d7c7d2f2cef41e5dc95dd86db7f2abbeb1f58c45d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d1e40442030765a3ac5d135c39154d052eba20953ea0e5d35a066f7722cdd93d`  
		Last Modified: Tue, 12 Aug 2025 22:12:36 GMT  
		Size: 49.6 MB (49641603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1cc20894541cbd711745752d2223fc23d38752d9fb22d82b12f78632b069aa`  
		Last Modified: Tue, 19 Aug 2025 04:02:21 GMT  
		Size: 142.5 MB (142460532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4630ba644b29313632b773d36ea30d91a0070f635392464eca3abb2fd92dc32e`  
		Last Modified: Tue, 26 Aug 2025 17:39:32 GMT  
		Size: 85.4 MB (85356612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7de4ef35ff3b1725bcc68922bf0bda777b571e3c28ce6491ef0bc1271da3bd3`  
		Last Modified: Tue, 26 Aug 2025 17:39:21 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:975c14989cd81fc86463752f18941ce70b4104c15bba6bd20e9f54323c3255fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11663d4a2d97c892fcb5f6e7b6e0ec4ee289e94394bf92bca6553067d66b50`

```dockerfile
```

-	Layers:
	-	`sha256:9a9727a237f1ba3df2e6124953c7bfe1e9157398c1baa2183ba7849771da081e`  
		Last Modified: Tue, 26 Aug 2025 18:36:40 GMT  
		Size: 7.5 MB (7490010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d55605d5d273b96b9c659450b68d63952503e842fa6b9b772708ba74f7f5cf3`  
		Last Modified: Tue, 26 Aug 2025 18:36:41 GMT  
		Size: 14.3 KB (14346 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:98a3bb6e468c11c503c85ff553c5cab0c056f91a75b63ada3a5589cd89a6b821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276899752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5352fe46e2435452c935662a42f8fe89e76048f5b41fba9a2dd7d95254a31ab8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:befe77620590f63939f5bcadadc9f45832981822c9c901f057eb4e86f733c29a`  
		Last Modified: Wed, 13 Aug 2025 00:32:04 GMT  
		Size: 53.1 MB (53103384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967a97862e5fba4f3e376cb8ef40e6f26a430a3f4696b51f2bc128f1d58140fd`  
		Last Modified: Sun, 24 Aug 2025 07:06:26 GMT  
		Size: 132.9 MB (132853303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d8069dab23936c2d1d039dff524ded06650dd99322e79ea4fe9ee415fed52`  
		Last Modified: Tue, 26 Aug 2025 17:49:32 GMT  
		Size: 90.9 MB (90942420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36233893fec70f54e69beeed9cd6a3e47c278e5775563d7f0178369576728429`  
		Last Modified: Tue, 26 Aug 2025 17:49:16 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:d4bd64b20d9418a770fdc6a3bb70fe437b7efbec7ca86929f15d3a0941511bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7500441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ac2a211973c9e0078a8ee8bad7d685236038e5f0bc2c4ee57cded9c545acf1`

```dockerfile
```

-	Layers:
	-	`sha256:0a052cd7ed7039f1e56953f02180ed5163d890c8b7bebcde2efe39d15127ceda`  
		Last Modified: Tue, 26 Aug 2025 18:36:48 GMT  
		Size: 7.5 MB (7486166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02de2099d0f1c20a3a9cf74c1a28d0da637836f8b210c304cd27c468910fc55b`  
		Last Modified: Tue, 26 Aug 2025 18:36:49 GMT  
		Size: 14.3 KB (14275 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4e7b44bfe3cf04df130f9e205b20a352a3e0d0ebfb9cce2565c09c3f6c5cc14e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.5 MB (261466477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c92e71022f867aff35864888662ee5a05f06283e27fe251cdd1e5d983acbb709`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1754870400'
# Tue, 26 Aug 2025 17:11:52 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 26 Aug 2025 17:11:52 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 26 Aug 2025 17:11:52 GMT
ENV CLOJURE_VERSION=1.12.2.1565
# Tue, 26 Aug 2025 17:11:52 GMT
WORKDIR /tmp
# Tue, 26 Aug 2025 17:11:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "68442caaeaaa0780957953dfac11278e3991d3baeb22579fc582ed1b2d5cd152 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 26 Aug 2025 17:11:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:c3b791adea90b39bc59919a9959b7f44f65aa3364a03dd0271a5ff658488877f`  
		Last Modified: Tue, 12 Aug 2025 20:59:03 GMT  
		Size: 49.3 MB (49345161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c1a2d3a2f2de1b60ce9f804a69133900188d6f67286a875440572a7d06126f`  
		Last Modified: Tue, 02 Sep 2025 01:48:23 GMT  
		Size: 125.6 MB (125622204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fd7fe2a51113eab35f0202a9c801bf6f0184c2737293a5297ec1af4d674533`  
		Last Modified: Tue, 02 Sep 2025 01:54:50 GMT  
		Size: 86.5 MB (86498466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8462feb0c8e03de1ce83a7c01563316e43caed0f62d93dfe9051c53318bba677`  
		Last Modified: Tue, 02 Sep 2025 01:54:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a7e139c173dc1788b83015b8c241574c257c6fa4aacdc193df4a9cb34519b47b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98f9b24ef7f9f498c8ae9f948b12f5dd120e7c10a55d45c6e564fbd080c39054`

```dockerfile
```

-	Layers:
	-	`sha256:e91ba588713c8c1a4955f2fea3d8d4ea1d32ae53132a02af3a21569322f94ff2`  
		Last Modified: Tue, 02 Sep 2025 03:37:44 GMT  
		Size: 7.5 MB (7478288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:057e6cdd5a614425ae2bfc4bbe13a9485500bc1ed2c8e5cf4651d8bca4f6a8a5`  
		Last Modified: Tue, 02 Sep 2025 03:37:45 GMT  
		Size: 14.2 KB (14228 bytes)  
		MIME: application/vnd.in-toto+json
