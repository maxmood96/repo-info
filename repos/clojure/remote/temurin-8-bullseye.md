## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:01f2c95111f09441e50a0ed3c4510579623d0c694030e81f99b34c68ffbe2c1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:def729b720c29291858177fa250f05c6eda10564112bf10439bb30bc04034414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.4 MB (230395068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de6fbeede640e2a7d2eafb4f44385a52372da5c891b0e725cb8eb53b13b877e`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a91183941977a3d5b9c6b26fa63038be9530c5c286feb444fda43596754673b`  
		Last Modified: Thu, 24 Oct 2024 01:59:17 GMT  
		Size: 103.6 MB (103634014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7530129aef98004970907c43a89707f3479e4db3ec4ae21ef38c905a8d525e55`  
		Last Modified: Thu, 24 Oct 2024 01:59:19 GMT  
		Size: 71.7 MB (71679798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b0620b596c595e88e61fbf5661bb8f6af20b532fc40b602b878366b44a52c3`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:85d6bdc41229397eec7895b4a1e022deefd95a2573ce7467dfda904b34774303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25300e251ce931444db12c29d5fb54050e7a49e65537dd295a768241c3e1d8d0`

```dockerfile
```

-	Layers:
	-	`sha256:d155e2b9199cbe387254c803d630bd26b5111963bb88ff4b7b202a677a63182d`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 7.3 MB (7338004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cf4f1f1412ad904d357551d059d6b3bc751cc39c7179188478ab7b9026cc0f1`  
		Last Modified: Thu, 24 Oct 2024 01:59:14 GMT  
		Size: 14.1 KB (14061 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3d413ffec1bbbaec1e58d62769628c740c091cbd730601957eef92c80f8ba9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.9 MB (225931734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ad853443bbc41fa9b528c042eb16e625fdc4ec41b60c6b5b46d6f9a308859`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5868f60870b916a798345f277a75fa895b849585a3f923ed55eb1471eeea76b`  
		Last Modified: Thu, 17 Oct 2024 07:57:44 GMT  
		Size: 102.7 MB (102729258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26345ada33427b07cd8f5ac0c2a284be9d09a893b0057e192749860951a42d9`  
		Last Modified: Thu, 17 Oct 2024 08:01:31 GMT  
		Size: 69.5 MB (69466937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9863219f2dd7b535a578e1c03ac33ddc38a2f09d171d20f3388197ae274049`  
		Last Modified: Thu, 17 Oct 2024 08:01:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8e46e4968839892318978e34d51c2f94c103420ea7513d87b9ecf3bfa0e6cc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7357978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5b1ec20df23c77917e17fca6dd4527be2829844f8c4911f21723225fd5aa2d`

```dockerfile
```

-	Layers:
	-	`sha256:42ab4e34cd4a72ba4206820611f469458edac00da1f7b81cd3de1ebc32066404`  
		Last Modified: Sat, 19 Oct 2024 11:45:12 GMT  
		Size: 7.3 MB (7343806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c13bc2c203fd7bedac4d316d2ca3f5eae626030f2ecc430354687832aa373c0`  
		Last Modified: Sat, 19 Oct 2024 11:45:11 GMT  
		Size: 14.2 KB (14172 bytes)  
		MIME: application/vnd.in-toto+json
