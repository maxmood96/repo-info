## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:17ab293d1bbba8c341e56fd3e9a2749631b8106d263402896ddc30ff83a46f59
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ce0c0bb0e9c6d2e5603d74a87579165f4df60442e0ba7e123b3ea839ec0ad4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67782932b212ac2b3d746faca59d6d0d94f9509da9b4c3acc563f0d2ccd85648`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5c32499ab806884c5725c705c2bf528662d034ed99de13d3205309e0d9ef0375`  
		Last Modified: Mon, 29 Sep 2025 23:34:35 GMT  
		Size: 28.2 MB (28228336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dd65c08fd455c903d4c6f53ca411e69d4212d328f8d351025df40b10717a86`  
		Last Modified: Thu, 02 Oct 2025 08:56:05 GMT  
		Size: 54.7 MB (54731290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a77f0242bd3cfbea01ac47c6ac04dac45bfa1b6a54e1790babcb1669d0adddb`  
		Last Modified: Thu, 02 Oct 2025 08:56:05 GMT  
		Size: 69.7 MB (69679702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd479fafdbe1c5fe2d421e33737cf057f25e62ab4b3123abc48119337601f4d7`  
		Last Modified: Thu, 02 Oct 2025 08:56:00 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3a290ee69934ade6175d9cd82e5aa69740dc7b5a49963dee8d88e9512af4ce38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9554f63ef44080517f885b25d697f6e70b8dec055c095a603f068f7626eccde8`

```dockerfile
```

-	Layers:
	-	`sha256:70bf0a821d872473bbaea0baf0877d2ddbec14608d5c1ad756f37f6e06ed219a`  
		Last Modified: Thu, 02 Oct 2025 12:46:22 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bc1ec91b81bd337242644c714f9d76a511a2710188ccc936ece629cffaacae5`  
		Last Modified: Thu, 02 Oct 2025 12:46:23 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c660f24a78c94858c6bf3652b9bf71cf0cfd5fc6615629f86b8b9e8a473b99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151498661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5643ac79299d5c2f83437cf6c4b0e2ae971927c89e64ff34bae44803836a5c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:f4e51325a7cb57cd9ae67bd9540483838b96bf7c9b0bf18205d9d30819e9ca38`  
		Last Modified: Mon, 29 Sep 2025 23:34:17 GMT  
		Size: 28.1 MB (28102145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8c231e3c0b7fd0d63c9176adacb96c2982dc2e7b87fb573a70c156d7edd5b9`  
		Last Modified: Thu, 02 Oct 2025 02:40:18 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69dcef46578aa606b7d4f1c8f2aada1fdd641f598af3dc489c9702289a1170bb`  
		Last Modified: Thu, 02 Oct 2025 02:40:18 GMT  
		Size: 69.6 MB (69560263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42c55e4c4a00e5b8a52beffc075b37317bcc96d3ced20b18abe857ed2ac41287`  
		Last Modified: Thu, 02 Oct 2025 02:40:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:06a4d161ce9e6ea1e58a65f6c62507c2407450826238d3c31de6caa47b64d56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32d02e66f21f9d11ac37f9494223897135997bdb98657046b068f35f71898ed`

```dockerfile
```

-	Layers:
	-	`sha256:839510eff6ce8f0325d3eb84d05573d81ac5e403e3c10b1b9b50759616a40003`  
		Last Modified: Thu, 02 Oct 2025 06:48:26 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85fa11111bdcf3ee0934f979a366b192533c225fb0ee03e19a705da064258bde`  
		Last Modified: Thu, 02 Oct 2025 06:48:27 GMT  
		Size: 14.4 KB (14407 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:3cc0463d1347816d6df4f5fe15eed9bcfda4a639b6e8da76b8905b1729c9240f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.7 MB (159747882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7da6c917287fda564fec99f480e2db942c49c297eb522a09202a6c0938abddff`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2dae4fd387571f8090d4bc2fed08c7939fa2ac7aed0e2814aea4306333899e47`  
		Last Modified: Mon, 29 Sep 2025 23:34:09 GMT  
		Size: 32.1 MB (32068697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf691ce5e6704b64a4e69f77604ca92a0653a44d6ab6c552f33638bc396beb4`  
		Last Modified: Thu, 02 Oct 2025 08:00:16 GMT  
		Size: 52.2 MB (52165419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d8768f0c73fbc58ebfe30d89f4cbcf0e1561679d3f317969eda66f51618241`  
		Last Modified: Thu, 02 Oct 2025 08:09:17 GMT  
		Size: 75.5 MB (75513120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a500d5dec4eace6fbaaff112f56834c37abfdf25fe7673e9bd28bd12514f2f`  
		Last Modified: Thu, 02 Oct 2025 08:09:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c94f0db804625ed0e859ad2068325fec8daf196e9a40cbd01106c5bcc43175eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c3cab92124ff285ed031914a3f134ffa16a52c94c79aa2642c5cb249ee0785`

```dockerfile
```

-	Layers:
	-	`sha256:59e1926dcf925ac0e423207a221d001fd67bb0cbf428eff60484d1de8b754105`  
		Last Modified: Thu, 02 Oct 2025 09:40:51 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd387e6631c6b5086ddd554f64e761de1256eba0008f8ea89ffd1f7bfbf53fd0`  
		Last Modified: Thu, 02 Oct 2025 09:40:51 GMT  
		Size: 14.3 KB (14339 bytes)  
		MIME: application/vnd.in-toto+json
