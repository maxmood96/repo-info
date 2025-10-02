## `clojure:temurin-8-trixie`

```console
$ docker pull clojure@sha256:227f658c797e7edb3c02a0d063efa8bfa9e0ae10a657eb81222337eed00f4599
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:2aeffea286f968b28b3a228b057718f192f42925743fe931369f86ffb74889a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189559068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb8465cffd0ca288fe8fca94f889cbc8b50e47a3e9419890848bd45ae0ef864`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
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
	-	`sha256:cae3b572364a7d48f8485d67baee38e4e44e299b8c8c4d020ff7fb5fdd97f88c`  
		Last Modified: Mon, 29 Sep 2025 23:35:29 GMT  
		Size: 49.3 MB (49284626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a7728e088e0c88e7a4ea5d2535dda35faaa30206bb1ad08412141d005f253`  
		Last Modified: Thu, 02 Oct 2025 01:50:22 GMT  
		Size: 54.7 MB (54731283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d44c7f84316a60429ddf4081089a76a9be4d86e4aa02b5ca0ec755a3cb9225`  
		Last Modified: Thu, 02 Oct 2025 01:50:32 GMT  
		Size: 85.5 MB (85542515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d34c3c081a0f2a20ae1303aecf07b2f1b18803436dfd3d4b55042913f539d9f`  
		Last Modified: Tue, 30 Sep 2025 01:34:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:c9a553992a88e7ba03792b77f0fdec5a7200857faf7c220d890ca44b95cce5c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07dcf70b3b08a3f5606d33bb8b409fa3f0ae717c2df569bbdf2c51f143d40a3`

```dockerfile
```

-	Layers:
	-	`sha256:00c0bd0dfe42e29c91e42c3defee793834babd0e0ab77ef2c578d075b873be7c`  
		Last Modified: Wed, 01 Oct 2025 15:44:53 GMT  
		Size: 7.6 MB (7588455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b04704927f8364a46492524bff28ddabf11f6129cd0f7c5e095371b2ffdbbb91`  
		Last Modified: Wed, 01 Oct 2025 15:44:55 GMT  
		Size: 14.2 KB (14213 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e3ca314e9c3d414838736c7e68e6734a63e9fae2009405640ab99ea8e25165e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.2 MB (192175489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d8ff8bdebcc014b1e9bf9b386a348bb6562593f6c09c46a0e684c650fdf212`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
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
	-	`sha256:28aec8b14b3eeacbf47ef38af72fab694b109fdcdf31581722750599baf1a932`  
		Last Modified: Mon, 29 Sep 2025 23:35:17 GMT  
		Size: 49.6 MB (49648695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d58c593997f72fdc61dbb01c6ed0a89e970af1c77b6e76d18b00bef5a4c84`  
		Last Modified: Thu, 02 Oct 2025 03:31:09 GMT  
		Size: 53.8 MB (53835607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29342fc5f8b1471a2ba4b812fe6662c0628ac411b1216646c2db58413fb0f834`  
		Last Modified: Thu, 02 Oct 2025 02:41:16 GMT  
		Size: 88.7 MB (88690544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53981a01908addfe566dbb7febfb7e810cdd44b28ec4a2a2e671dab218acd833`  
		Last Modified: Thu, 02 Oct 2025 02:41:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eab78aee19cf740affbc5934ce811b89d293f73b0d144fa70d40ab96f51db016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cbcade19a69daefcdbad92ce893143c85cfa43b412ce13159c7d24e5f4001d`

```dockerfile
```

-	Layers:
	-	`sha256:65d271e8bc0dc86268fcff44afd0a6e0aed645e5c8e06ef71cac46e00d607ef3`  
		Last Modified: Thu, 02 Oct 2025 03:37:46 GMT  
		Size: 7.6 MB (7596237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108d4fce546e2b5b477f922a8982b99ec8b0decd7f6f8b8800fe4a9f64acc8c9`  
		Last Modified: Thu, 02 Oct 2025 03:37:47 GMT  
		Size: 14.3 KB (14331 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:916a68aee4039067029275716e623e748ff5b4022cdd43e614c58e92f28c9ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196223559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49cb88e0a518737c3ca1eda3b57196f30aac4243582fde6d4ea10c12ca563c95`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
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
	-	`sha256:71fbf24a239310917388930bb043e64907cb532b9ac8f265e44e032dc3bf4409`  
		Last Modified: Mon, 29 Sep 2025 23:41:05 GMT  
		Size: 53.1 MB (53109217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ea20399e26207a7161dcbba70b3d1dbdadc77dd9c3314c9940ef2d48c2b8b7`  
		Last Modified: Tue, 30 Sep 2025 13:30:24 GMT  
		Size: 52.2 MB (52165414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9304da3e03017a2d2f366f441de3e29005cedb08959d4de6fb7181f7e9302e`  
		Last Modified: Tue, 30 Sep 2025 13:35:14 GMT  
		Size: 90.9 MB (90948283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e897fbf1e9e442e86dc20fb6880021a54edcc09bbb0c95166de8e32fdd2447`  
		Last Modified: Tue, 30 Sep 2025 14:25:45 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2b2c63cfe4e31a3f2c2002fa6fd3ae850b9bcb9439d3fe7ddc01f48dec203c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fe8c72f717ef5ae491c6fee6f3011e9aa620caebc03e72ea7f60b2771761193`

```dockerfile
```

-	Layers:
	-	`sha256:f4e6927dca3cc1fcb705cc35b5f5a5229d4c8fc30323866c3adce8dd20514094`  
		Last Modified: Wed, 01 Oct 2025 21:48:25 GMT  
		Size: 7.6 MB (7593467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31771a948428b1faf31b0b2d46ac8614b37d96c627ecdd30c50ce58563ae5677`  
		Last Modified: Wed, 01 Oct 2025 21:48:26 GMT  
		Size: 14.3 KB (14260 bytes)  
		MIME: application/vnd.in-toto+json
