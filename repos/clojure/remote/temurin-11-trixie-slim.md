## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:c8474a24a288baff6faca51dfbb7cc9029bb5bdcd1350fa014c38ba82f33e297
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
$ docker pull clojure@sha256:a3b51e9341266105adb2fb8bd9f4cbc8a4bcade40b385a51f279e17dd228886d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.6 MB (247595439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c344b7dc2cdf93f5015c7354af472207d9521bcc84dfdf13a5a21d0ce0c20d8`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 02:57:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 02:57:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 02:57:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 02:57:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 02:57:38 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 02:57:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 02:57:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 02:57:56 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5608634c2935e7934356895f3ae794066fea3be535b1554ce591d6ed30e4a39`  
		Last Modified: Tue, 17 Mar 2026 02:58:21 GMT  
		Size: 145.8 MB (145806912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f02bd53ce531ca11e2f6b1038a0382ea138588cfb536930f9526431f1b61be1`  
		Last Modified: Tue, 17 Mar 2026 02:58:19 GMT  
		Size: 72.0 MB (72012383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874976330358fb05bb3ae2aacb1423247ccb1886c2c884e7ea8a58bc391edb52`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1f54b1331c15ebbad94a99a61af146b9e763455038bd2fe014dfe68180cc130c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5293522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bf0454f92c786aaea5dec9331ace8f4f0a86d9e7b74c9089054531f047fe9b`

```dockerfile
```

-	Layers:
	-	`sha256:af930f28cb786f2e86bc22fe366a611c3f348e7b71060f4875fbdc6f519bb303`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 5.3 MB (5279279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7fcbd386018aa65c9653ca08082b06f0d4342c260855249d429fc07d2057a2`  
		Last Modified: Tue, 17 Mar 2026 02:58:17 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:064d45e3124b2665a962be7c6f5e9561173f0660796e99de34aa40691479ab46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.5 MB (244470463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea7f1bdb0b4abfa77d3bf0421ddd6c76dfe48cee729951851084ea0cf3c2285`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:02:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 03:02:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 03:02:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 03:02:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 03:02:10 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 03:02:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 03:02:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 03:02:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c163612247ce9fd6f679f0c5dc6a860a98a193594087bd66b1c30e5840a5346`  
		Last Modified: Tue, 17 Mar 2026 03:02:55 GMT  
		Size: 142.5 MB (142500051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d49927905650ab5f9dde5dde2a7dbc3eb7c11374575a3a5d09d18e67a61a5797`  
		Last Modified: Tue, 17 Mar 2026 03:02:52 GMT  
		Size: 71.8 MB (71831353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0e4347d0b09d6ecd09d8b5ce6875afde466916ea030365fd04751ac8f2b429`  
		Last Modified: Tue, 17 Mar 2026 03:02:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fdf800debdf41a171fad4e9581dbe7dbb14b67db60c66a1eb00fc20cb669e824
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5300027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ecc2291b725f771ddebfec965d519985aa7bea2836b2d429f012d9c51fc5b6`

```dockerfile
```

-	Layers:
	-	`sha256:1d5f5c3536f2b29eea84d4eb1f1aa70a3f1d691765b1b1768fcf37cb69840c05`  
		Last Modified: Tue, 17 Mar 2026 03:02:50 GMT  
		Size: 5.3 MB (5285666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:055fe0812e8d4f8c32e0592241c750c7ea2054e10818197b43ceae4f4e606a0c`  
		Last Modified: Tue, 17 Mar 2026 03:02:49 GMT  
		Size: 14.4 KB (14361 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:32281b7c02956fa335e30a40026ca1afea9449d62538aa08d990a4c7b6e639db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (244019330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bb8e966432f4acac977a142dcad4f4ef0efaebfe003b6a212eeacecfd7cb154`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 18:18:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 18:18:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 18:18:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 18:18:16 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 18:18:17 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 18:23:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 18:23:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 18:23:49 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6d8bc187d9d77c2b576c45cef2edbe313dca76b0d35a49ca751f0587487fda`  
		Last Modified: Tue, 17 Mar 2026 18:19:41 GMT  
		Size: 133.0 MB (132996714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53b836d66d91e22b570ee107eea8357b31cd2c26e0469e1f67f84350aa4f2da`  
		Last Modified: Tue, 17 Mar 2026 18:24:25 GMT  
		Size: 77.4 MB (77429143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7ff01b39ee4c05cd706d2f9bf0d4a1dbbae99b7defee725941e89d3f87c0a84`  
		Last Modified: Tue, 17 Mar 2026 18:24:23 GMT  
		Size: 607.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:0db2a626d04fa56858774dcecc2047251dbb0bf3a319cc49c3e47a6be847254a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9334f39c04b16986ab17dfbc57da78bd0d62da139b5c702c20f1cfd7db5eb65d`

```dockerfile
```

-	Layers:
	-	`sha256:39d905225768cc265235581bea62f63e27a380ecfcdc3ade7eba98f930ec7291`  
		Last Modified: Tue, 17 Mar 2026 18:24:23 GMT  
		Size: 5.3 MB (5283035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c77308363b15cb7466b2a19bdb01aeb028f7174152743c643edbce642fb80329`  
		Last Modified: Tue, 17 Mar 2026 18:24:23 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:07041bd2987a7ac4f370ebd75604b85c5a3f8b19f31256a5b014b6d93ce3c793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.4 MB (229384679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3353610c19fc3e52b3056cf5c393497118ef35562ed6ac0486f78c040d4026`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 11:32:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Mar 2026 11:32:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Mar 2026 11:32:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Mar 2026 11:32:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 17 Mar 2026 11:32:18 GMT
WORKDIR /tmp
# Tue, 17 Mar 2026 11:33:35 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Mar 2026 11:33:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Mar 2026 11:33:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d8963bef282a595a41b68d963937dd1c89bb63b69a25a59d5b1729d4a2fafe`  
		Last Modified: Tue, 17 Mar 2026 11:34:26 GMT  
		Size: 126.6 MB (126562115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f75bc7f31c187ebcabd24478abe5b7e113931f80d641f523b505d461a937a84`  
		Last Modified: Tue, 17 Mar 2026 11:34:25 GMT  
		Size: 73.0 MB (72986655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6c2d8c46584d6b2b79003f88599c88dd7fbf02a3e74b24f44121de0ed729be7`  
		Last Modified: Tue, 17 Mar 2026 11:34:22 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8967becf1f7ed27c919312176462d78a6e919a783d936cdef119dd2bb95ff7c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3a84793488871629346e532f9e1ca913991c0c47a24a4dbcabfa48a73fbe35`

```dockerfile
```

-	Layers:
	-	`sha256:21824d5df6336bb314394bea58df6c0d1923a90f5c6c5900e697795bde0ea173`  
		Last Modified: Tue, 17 Mar 2026 11:34:23 GMT  
		Size: 5.3 MB (5275207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80ecda594d43b124ff27e79ad67ac238430862f22025534c0f0d0633a3a527fd`  
		Last Modified: Tue, 17 Mar 2026 11:34:22 GMT  
		Size: 14.2 KB (14243 bytes)  
		MIME: application/vnd.in-toto+json
