## `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim`

```console
$ docker pull clojure@sha256:90fbd2a7c5eb996de3e85d0334c87bb2be50b3501a751386d34684525b9ab90e
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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ca6373668d4918a22974bec57e01afb5a1bc347d408aa4934459d4bbf5040a05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239865597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c248141ab50074711e5347a9c91942520325b4783f4efcd47e8df1ca93a834d`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b722f6de86e72fb07562d87346af6be7b90ba50431c937810c2662421c09c4b`  
		Last Modified: Tue, 06 May 2025 00:24:11 GMT  
		Size: 142.4 MB (142420712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d416fdf94bb484a65be64d1223f74a51d43950c0bde73a208fd7a009eb383b83`  
		Last Modified: Tue, 06 May 2025 00:28:46 GMT  
		Size: 69.4 MB (69377617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce6506d3a9ea7b8021b4047bd5130e489050fb60813a32f6d04ac48ecbb8e7f`  
		Last Modified: Tue, 06 May 2025 00:28:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e75052942ac47bae7387406b838c62e909fdc967a13ec68ce560af01eb0e53f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4954913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f87bcac3ef14de765cfaaf7eb210d451ee9bd6f03b7d3e8240119875088942`

```dockerfile
```

-	Layers:
	-	`sha256:5e4a54ea5c322f6c5a184d4cdc0af790bef02094b8df2a3b3cb3cad64bb36d2b`  
		Last Modified: Tue, 06 May 2025 00:28:44 GMT  
		Size: 4.9 MB (4940485 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81fc09ed8ab262e32294a361e0ea931bd007a995bd60ba4eadc4440d7ac7c965`  
		Last Modified: Tue, 06 May 2025 00:28:43 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; ppc64le

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:3641326a5600aa59f28d0b090acbcf692775cbfea200678589f1607309829091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220804277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3cb514575428099dbedbf751118f20a392150751ab4e74b37f63fa596b4f4f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
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
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69538b52f7425848b38148059ce12431efaa1d2cc2a4a2afd2bc04d9521e6283`  
		Last Modified: Tue, 13 May 2025 17:56:43 GMT  
		Size: 125.6 MB (125585845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1ad5db217be43270e2455dce10bde40574ef941942768925674ccbdca55597`  
		Last Modified: Tue, 13 May 2025 18:02:59 GMT  
		Size: 68.3 MB (68332922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637924786e5ba924b524a31a7a653ca903953662bcbccc3b6c7866f403546a5f`  
		Last Modified: Tue, 13 May 2025 18:02:58 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:66dc7f7fd3133cead3c8ec856cc49f9756bfc7035cc3d91c791cc5f2abef2324
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4942633 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c5380a1378141d9b83211047f0a57c3b17828be0f06c31fbed6b5759c062da`

```dockerfile
```

-	Layers:
	-	`sha256:91d8f070722969f8d5efbcf6b26b02e4b11f6197e8bc33833a4ae368eff4c67f`  
		Last Modified: Tue, 13 May 2025 18:02:58 GMT  
		Size: 4.9 MB (4928323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d04fa97e3f1791db183fa61dcfc9d4d058b7e5b88f1a4a7b641e775e64b2eca`  
		Last Modified: Tue, 13 May 2025 18:02:58 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json
