## `clojure:temurin-11-bookworm-slim`

```console
$ docker pull clojure@sha256:a6311dda3f2152b39d77b23f7998bc4478aa41a669a51739a5e44312b70e2164
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

### `clojure:temurin-11-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:82bb8cad39cd225d8b25105627ea33dcee0005dd54ad33019ef8f0faa80b3cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.4 MB (243392559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fd760fa7bfe53ebe97f6cf46a5bec815a071f0b0790dfc746ef97ee6ad6e363`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c334ba08ed2fb69d58679a953992a7f4f9b91fb2d001c01ee51cdd6e80b4c`  
		Last Modified: Wed, 21 May 2025 23:32:26 GMT  
		Size: 145.6 MB (145635749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7ac8d6dd45327dcd864edba5f930e3a9266ef55e805250492c5bc15908db5b`  
		Last Modified: Wed, 21 May 2025 23:32:25 GMT  
		Size: 69.5 MB (69530835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017204c092ecc9ee21ab7addce80b11919e0504626764726351bbacfb85c4a68`  
		Last Modified: Wed, 21 May 2025 23:32:23 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:4d387e32e5a729d5bc83a26991f98361092f5909bc5f800e81139505b7fe1bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4995949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adde3adbabfe8698a523bbc9e4578fc0528e0c866e94a2488f4dfe46007aee29`

```dockerfile
```

-	Layers:
	-	`sha256:90a2e575924470a330cba910907605a815ef2017cf24225b7330b000703b6365`  
		Last Modified: Wed, 21 May 2025 23:32:24 GMT  
		Size: 5.0 MB (4981639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b5efb637beb714d29a40c6349023fbdc9c414e99cc88c1275084574b7d60ef4`  
		Last Modified: Wed, 21 May 2025 23:32:23 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a88cc3cd92789a987b1015429dd2f179369c42e34255feffdaf3377cd2c4011a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239872845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97032dc7096f711a87b8f568deceb5672ac4bc40ace1ba33a8abc96266ea3ce0`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37350b9d182fff661b148558da9ed47009fbedca9d38d8cbe480308ffbe9b84a`  
		Last Modified: Thu, 22 May 2025 08:10:24 GMT  
		Size: 142.4 MB (142420719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766e65a46986942725e25a8a7fcd04a446ae993e92ec50a004d020914a5c161c`  
		Last Modified: Thu, 22 May 2025 08:15:18 GMT  
		Size: 69.4 MB (69386203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8478739e911f82c5885c32677756ba959b434d38e903a1dc7cf81692e2a9a6`  
		Last Modified: Thu, 22 May 2025 08:15:16 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:25e5be6e0bf010d9e3c225512e4325131660b35825737e3af458f8e6e17c4f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5002445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00a4e4d71c2048e760d73693ac070747cd31b307af37cd13e0cdb7089db951f2`

```dockerfile
```

-	Layers:
	-	`sha256:528133687a6b54982f06d3dbac5ab32d8512577c51b40ce54006b9a9c2607a58`  
		Last Modified: Thu, 22 May 2025 08:15:16 GMT  
		Size: 5.0 MB (4988018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cda083903af58f89db7048ee495a33a7dd480acb407c00dc1a3bf4f1b30aac9`  
		Last Modified: Thu, 22 May 2025 08:15:16 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:21726ec2b6ca1fa04d4fb072bbc18d506e6e5d94dc2e6987c8bb3c6b7e2017d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240223649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a6c6484ea7099959ccbfb981526d6def0ccf22bbd7b57e635977a7b3be1bff`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
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
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072938722d633c364ba2ea6b70c7a07f710edd3b5fea7decbffa42f42997ea3e`  
		Last Modified: Tue, 13 May 2025 18:27:25 GMT  
		Size: 132.8 MB (132809833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcf8fc3d2afc29519c84eff8c8ab0995b1b914983f23847abc4e9d82cec1a51`  
		Last Modified: Tue, 13 May 2025 18:39:42 GMT  
		Size: 75.3 MB (75344729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b08a051687b8fca8a062f9bac832f88e46dc0cc8b4ba3d3b691a21f00c7edc`  
		Last Modified: Tue, 13 May 2025 18:39:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:801779e2e872cbb2b25bb13e68b38c4715d2f84fe5c74d66e7c311d1b5582903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4952841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a36faa752141e70a583d74a2a49f7aa3dc558b9949f547ed496664145fd194c`

```dockerfile
```

-	Layers:
	-	`sha256:7028cbb2bc0309f442f7c6a086b53202c0ea90e36769eec8976652dbc4c82df9`  
		Last Modified: Tue, 13 May 2025 18:39:38 GMT  
		Size: 4.9 MB (4938483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28c36ab07ce5e9b3a8e449179a5685bd834a402db3dc2c884f6be19b815d7e70`  
		Last Modified: Tue, 13 May 2025 18:39:37 GMT  
		Size: 14.4 KB (14358 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:b6078ddcf5162272abb690330dc5c652915263a8fc57d7524a0d1074773f660d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220796580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2fce47fef1404f9ec3b54ad30bca95b8a62b4d5553181372b39fd3a1229159`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
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
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8320f723c77b813fa8f45308ad2223914b761653eab90015935672d843c1787`  
		Last Modified: Thu, 22 May 2025 03:39:39 GMT  
		Size: 125.6 MB (125585847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b81a6e438fccae1727c43b6c89db99c8b24a1eebedcbec80347e3901116ca31`  
		Last Modified: Thu, 22 May 2025 03:43:31 GMT  
		Size: 68.3 MB (68327280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ab755cc9f4c1f4337f7853162da292db6bac5445cb9a4d91e04e7f48dee110e`  
		Last Modified: Thu, 22 May 2025 03:43:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:268098a9f83c4a2264a9a272105e464fffb70a878a2bfdd6a1b0ced4b538abbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4990164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:756877af6c95d67557c17abb88fc2a30c0d035cf91d15bb2a82f8143cf5617ad`

```dockerfile
```

-	Layers:
	-	`sha256:8b227673e81e5f561160bb9b784543412576d45a0beb5c65e3f1a0d5efe8deda`  
		Last Modified: Thu, 22 May 2025 03:43:30 GMT  
		Size: 5.0 MB (4975856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8270dd1ef086b39065d49011710101c54a0ca8fa8e57b845e5adf17a20a5f44b`  
		Last Modified: Thu, 22 May 2025 03:43:29 GMT  
		Size: 14.3 KB (14308 bytes)  
		MIME: application/vnd.in-toto+json
