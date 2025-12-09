## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:b3c873ea573412bd3386b13675a8c50740eb0fd492753c3d871b9b8c640f3349
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:805c7b108e6ef3d855e8ca31dc0f589687fc9065f429c1c83568cdc45d46619f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.6 MB (189564866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cdc421efac734cf02c83b7863562fc986004281c96d080b238d2b68e583cd18`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 06:05:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 06:05:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 06:05:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 06:05:16 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 06:05:16 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 06:06:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 06:06:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 06:06:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:53c88f1dfeb79b2f207f7f1a03a45e0dc5ed208b9f496de16b98f81189dc0392`  
		Last Modified: Tue, 18 Nov 2025 02:34:19 GMT  
		Size: 49.3 MB (49289547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa25699c93dc7bbeb34f328faa846ea6e7aaebd3e2103f6a7415ab228753165c`  
		Last Modified: Tue, 18 Nov 2025 06:06:00 GMT  
		Size: 54.7 MB (54733389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43eb51414ba78d81977edde665aab5ea3df9948185f3b0f92627dd53acb7d19b`  
		Last Modified: Tue, 18 Nov 2025 06:06:56 GMT  
		Size: 85.5 MB (85541285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa98989f385b508931e4268476af7cd7b2e44d7ad051c4cdb3355ada5500ca0`  
		Last Modified: Tue, 18 Nov 2025 06:06:47 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:05fcc8009580ce3c15e5ad27e2295b73ed86346449e9236d52cafe94459bda9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7602709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95ce9882f5fbcf29891a682541c0113dce889847a4c22d4b3c4c610b7e82b12d`

```dockerfile
```

-	Layers:
	-	`sha256:68eecc62022b065f87d6ae9a1b873e1f79df78e093b329898cea1f74b43504de`  
		Last Modified: Tue, 18 Nov 2025 07:51:20 GMT  
		Size: 7.6 MB (7588539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b640f335b5f7add7c824c48993efa4a4e5c0806ef5d34c9102ac0847e7c6ac58`  
		Last Modified: Tue, 18 Nov 2025 07:51:21 GMT  
		Size: 14.2 KB (14170 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:56b9365f6f2da6cda0122716b4488b36f8f101a06f8b992edf570a8fbb4060cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188830580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56655f7a06d928ac59701b54a81a960bc5251643c015cd5e7dffda09fdf91da0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:54:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 18 Nov 2025 04:54:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 18 Nov 2025 04:54:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:54:55 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 18 Nov 2025 04:54:55 GMT
WORKDIR /tmp
# Tue, 18 Nov 2025 04:55:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 18 Nov 2025 04:55:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 18 Nov 2025 04:55:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9276e76e62afd8421516059c0238d0d2bba58227af1cbce32b43d67781151ea2`  
		Last Modified: Tue, 18 Nov 2025 01:14:17 GMT  
		Size: 49.7 MB (49650232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d390101a8f55dd574426378320adc57b317b7d2c43dd7873fdc952d32c4bbc0f`  
		Last Modified: Tue, 18 Nov 2025 04:55:45 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6720f81e97a3fc85826592062d73cff1f275218ce9eb9aeb139d43cb1723f95a`  
		Last Modified: Tue, 18 Nov 2025 04:55:44 GMT  
		Size: 85.4 MB (85364704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c1d0ee4857da2b139e07757eb24f7cdadd235c863cea189f177d2555af987`  
		Last Modified: Tue, 18 Nov 2025 04:55:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2c3754f9d7015ef3414290ecfef8efabc7705dc7bb0ba37ba0af12f1aa507ae3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7610555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20bcef8991e2419189d5ee1785f3915d89dafd522b211cdbdcfe645e104a4c21`

```dockerfile
```

-	Layers:
	-	`sha256:215f12de1f83ae166bcbeb2ac3d014c4dbdfc98d0b59c19b3ef140e1ff76c170`  
		Last Modified: Tue, 18 Nov 2025 07:51:29 GMT  
		Size: 7.6 MB (7596267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f485552a7dee6d3cb9bfdd141fe06b8dee9af69739515b815e1e8a1f6a5e47a1`  
		Last Modified: Tue, 18 Nov 2025 07:51:29 GMT  
		Size: 14.3 KB (14288 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:3d7c652380bcb790ec1e0d1e6fe10a1f2d510726501c3d0f0af936e455d340e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.2 MB (196231755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43e2bd645c8132afed74a78a94bf3e5d437d9ebd3496fdedf880e9fbb097e87a`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:23:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:23:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:23:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:23:38 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 08 Dec 2025 23:23:39 GMT
WORKDIR /tmp
# Mon, 08 Dec 2025 23:24:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 08 Dec 2025 23:24:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 08 Dec 2025 23:24:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17fdcbbf285191165c95df89028a64259c84d1fd6873060f7cabecc5d7fc9547`  
		Last Modified: Mon, 08 Dec 2025 23:25:07 GMT  
		Size: 52.2 MB (52175122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891082bb1e05c9f765795b20d511d6918e35d2c66b3fa35cac6d0cf82f2f621b`  
		Last Modified: Mon, 08 Dec 2025 23:25:34 GMT  
		Size: 90.9 MB (90947510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c51f681687c5faef873c158dec7b49022fd212fd741588e52c23e5f7a6d6fcf`  
		Last Modified: Mon, 08 Dec 2025 23:25:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a7f89413e7061312579462d8852a9e21765411efe397cbe55cd6b6d21bd8dc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7607769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c716a2729ff4409086fa5678b3ae1740cc919e1a7a145391a8baebd8563202`

```dockerfile
```

-	Layers:
	-	`sha256:b29ac7da0ce764f7d575cf00cfb8ab1c5f3291b386fe2c427107aad6bbdc9fb2`  
		Last Modified: Tue, 09 Dec 2025 01:40:42 GMT  
		Size: 7.6 MB (7593551 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fe46faca7a03720b687c1aa8996b90446cae1a0cbb9e970118c4416f30332a0`  
		Last Modified: Tue, 09 Dec 2025 01:40:43 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
