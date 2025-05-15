## `clojure:temurin-11-trixie-slim`

```console
$ docker pull clojure@sha256:59c01282237bc191cbe05cd2f5420b076d7554e3e6e74fd16912291315b229b0
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
$ docker pull clojure@sha256:8f851b6661ee3e0189218dbb665882f416ff256209dcc178767e426d274db017
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247114236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:635a819ae4ca5d703b77c6002ecdeef91a14776ae9d26f1e2d9f901dcc5fdecf`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:3ae34fc80ed56f2b3a9a0b682b58e28e57fe981f5e514c3f687044f4b967608f`  
		Last Modified: Mon, 28 Apr 2025 21:08:25 GMT  
		Size: 29.8 MB (29753912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd5745ef7daa46a3fa457e61f66ef1f081deaa7423b90c21d6fc53c01759030`  
		Last Modified: Tue, 13 May 2025 17:54:12 GMT  
		Size: 145.6 MB (145635736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6b50ad1e24a35aa678080184c3905f8f37675fa2b38c235198e17d81786808`  
		Last Modified: Tue, 13 May 2025 17:54:11 GMT  
		Size: 71.7 MB (71723945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f4ea736edea8b42d66c45d10fef72125ce7984bf448828c0707c4e69024135`  
		Last Modified: Tue, 13 May 2025 17:54:08 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c0c853609b419f22c10ae920d8b96f233a208d936d0352fd54c162d87fea66ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5101114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3862f8a946f5e01faae5326ceb869ae4081f0a0dbed405b6112be97680cfdd94`

```dockerfile
```

-	Layers:
	-	`sha256:7bbc4d427e6e4f3c07a913d14c9d4ee4e6839f6479aa77dde77ee88695557f7d`  
		Last Modified: Tue, 13 May 2025 17:54:09 GMT  
		Size: 5.1 MB (5086828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9eff0d28a7f433aecc2ba9014ff8e6559c5cb2e58171ad21941b121c7d13d324`  
		Last Modified: Tue, 13 May 2025 17:54:08 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bfbb2665f4137528827357ded9eecc55d9cf5e424e6cb70486e221218dd4436b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244197534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a27d4e2dc70da51495f784cf3f7ff80ac230bda9cfed1a3dd2fad9f47a63d58f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d0342bfffaba1a8be0950e44b5334c6cf9a05d9eedd81a042ec7813ac91850a4`  
		Last Modified: Mon, 28 Apr 2025 21:23:36 GMT  
		Size: 30.1 MB (30130233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394cb701603cc841d1cc1d1ad27378dbf17582cee266d468265a01aaae9a60ec`  
		Last Modified: Tue, 13 May 2025 17:58:05 GMT  
		Size: 142.4 MB (142420736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393cfc287c1fec5cb904c2221ec15940d11b9ea9f04aec2841bacd2a7e5b73fe`  
		Last Modified: Tue, 13 May 2025 17:59:37 GMT  
		Size: 71.6 MB (71645922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3c8ba0b83e12be14fa152d6899f0aaaf5a4c68accafffa97ce9326f8fa74e7`  
		Last Modified: Tue, 13 May 2025 17:59:34 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:103e8bba03e1614c8b06cbd3ccf3ea03d457164f6f7f79f36920bd7a5e67d8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5107619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4a6d778373ec6a44ee65d208b313259518900e42b253e63ec735547141da238`

```dockerfile
```

-	Layers:
	-	`sha256:91b814dc4fa77865e12c16dd2dab3a61655473a0ddcfde973695a5c43aabe9b7`  
		Last Modified: Tue, 13 May 2025 17:59:35 GMT  
		Size: 5.1 MB (5093215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:181e1fc63cdd84e1b617db6026b8c5bebf8e24893f621ad31972e3913341e05a`  
		Last Modified: Tue, 13 May 2025 17:59:34 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:875079d23f1ffc92b26105dc7846a70aa37ec22a0c5f5e2a2c1148849740817b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243603111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0262f0782a2f7c896b0960b00b7cdf31c56c9db69cf2e026ec7ebb5dca694d2a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a739447e8599431e1e4996b4b6d4022822d37eddea9a3737acbea74b8a860d49`  
		Last Modified: Mon, 28 Apr 2025 21:25:59 GMT  
		Size: 33.6 MB (33577694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a20e2c1dae1640014ab6fa85e5ac56c9c5b5992d7ee7e9a915c99170e00b082`  
		Last Modified: Tue, 13 May 2025 18:36:27 GMT  
		Size: 132.8 MB (132809819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ddd2a9991975868081fd8778e0a275e861cc167aa874b9546dd572d966eb710`  
		Last Modified: Tue, 13 May 2025 18:46:07 GMT  
		Size: 77.2 MB (77214953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b79bb657146c08440601faae799bd316eef44bf2d7af3110ac9d386d88d239`  
		Last Modified: Tue, 13 May 2025 18:46:04 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:dc145cad3db0d9db8a57658c1b8fbfc4dcb766f59a135ae9ec49e359e8a640a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5104756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab4ed3739991f0245817a8ea11bf0baf308bbbc508ea3e644b2d650df9321cb`

```dockerfile
```

-	Layers:
	-	`sha256:f98bd96592c0131ba7887d02ef4cf6a242327364adf8ac7fa3159aa7acfe30b9`  
		Last Modified: Tue, 13 May 2025 18:46:05 GMT  
		Size: 5.1 MB (5090422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1daabc892a0400ce31f0b9f94e389d98ffbeb289f442f1263e17afc19fed70b8`  
		Last Modified: Tue, 13 May 2025 18:46:04 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:95888c229b2c554024aa48d1400f7033198bd9e8154e05f0e3965629de3b6af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228225349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0095f7f916da139f2ea8e4fffd22e43e39f2426991824200989ca11be388694b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2efa8ce97d282fc76ea2985fc31102becef655447ddbf9bdd3209771347a0182`  
		Last Modified: Mon, 28 Apr 2025 21:11:27 GMT  
		Size: 29.8 MB (29825462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f615f52726f923dbb1b1725bda0476f67948d69a154a2121e2d7131fcc80f55`  
		Last Modified: Tue, 13 May 2025 18:01:01 GMT  
		Size: 125.6 MB (125585845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81dfd9fe585305797a89a003c444a48fd5e7af7eae81763b628ac899125e3bc2`  
		Last Modified: Tue, 13 May 2025 18:07:21 GMT  
		Size: 72.8 MB (72813398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e4e8175845fb01d1e5db91fd92b603da6d7130b9df6b4a544b2979095e449c`  
		Last Modified: Tue, 13 May 2025 18:07:20 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c56e456a45c1e4c62b8b0a1ecda9144ad1ffeda5e417789965d6c0404b221986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5097042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52cbe80fab9bb5d07eec6f1188926ca8bf751d38e0ff38a5154a51f519514633`

```dockerfile
```

-	Layers:
	-	`sha256:f5ac27cb4d67f5ec88c14d276f3e547489b169ef61ffdf6cfa802f187291b50e`  
		Last Modified: Tue, 13 May 2025 18:07:20 GMT  
		Size: 5.1 MB (5082756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd33a4c5179ab065c82e95f4b9080328580a8b5fed2ae487f2ccb3077541fee`  
		Last Modified: Tue, 13 May 2025 18:07:20 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json
