## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:8365ffb3e1459e32bd2ee5f905818f47e4843880ccb0f3e0c2cbe780122cd978
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a4eb10779b6b72be6514d5fb452f9da308a106e16e57a049d468f582ff63795a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bc62724fe38fcdde9d896198c1e5d4531d174ab30ae4fcecd83c4ebab769a14`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4aebe6aa495a52f6410fec3417c73614d4437cad01e2bf88756def8d3ce98a`  
		Last Modified: Fri, 27 Sep 2024 06:01:10 GMT  
		Size: 145.6 MB (145550047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5026bcc9b4abe91a64d115fd4dcd235d59c52d056d95606bca1b1a13f36222ba`  
		Last Modified: Fri, 27 Sep 2024 06:01:08 GMT  
		Size: 58.9 MB (58940207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b4681c9d811d3557009f1edfa351673250576451cbf65f8024436f24281084`  
		Last Modified: Fri, 27 Sep 2024 06:01:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eaf0a4e498f92999e0a05f952a4d2bbdac179c2ddaac62c86d74d53bf7aa23f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e2a61872f10a13dd8753bca9725eab5e846012e000c705f82f49a6124266f3`

```dockerfile
```

-	Layers:
	-	`sha256:afeaa945a9c6ae6c9233b485c76238776ae377d8fe737faf1d51ef204fc2af3b`  
		Last Modified: Fri, 27 Sep 2024 06:01:07 GMT  
		Size: 5.1 MB (5119616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f48616cf4db95aa7fab7741adf9f17641f0ee0a2ef668d59516e6d3d94767361`  
		Last Modified: Fri, 27 Sep 2024 06:01:07 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9733ed3c49eb1dafa9d44211967754a89cd210bf1d34cd94f405da272a4a9847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231501505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd73207724a5b8943bbde59d36fc030fcb672460ca185965fbc52b26b5be70e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:40:08 GMT
ADD file:0802ca323252c154049da951c7da8572fb921f823341726dd7664f05c009e50c in / 
# Wed, 04 Sep 2024 21:40:08 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:172514850d5c3a8b3bc66fd0f1f345729d1b0b249cc3f053febcb64a066835da`  
		Last Modified: Wed, 04 Sep 2024 21:43:10 GMT  
		Size: 30.1 MB (30074365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ef10236f25c95578237050ed53f6354899cf160fc8f9a9086ee3d535960c3f`  
		Last Modified: Tue, 17 Sep 2024 04:21:34 GMT  
		Size: 142.4 MB (142354751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca58bef7c40bb17933b2c733330f9eece2904631d261f9c2a4ad06848301f899`  
		Last Modified: Tue, 17 Sep 2024 04:27:30 GMT  
		Size: 59.1 MB (59071742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdeb45d8d2490e32fa3e6b4f073a67b8a8ee51016d52459081006d7cfa7fb9ad`  
		Last Modified: Tue, 17 Sep 2024 04:27:28 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e49eb645bb55d4ddcb33998fd220639877058453a1bce6080c238d5983694905
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4970661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf91b69e81b712f2c6d5d75259cbde6f5d6cff8c5ff29385ad71086d32abeaf`

```dockerfile
```

-	Layers:
	-	`sha256:e53e31bc116fcb4dd3b9da297580c5331ff988b08a35541cc841d9f3164ac8f1`  
		Last Modified: Tue, 17 Sep 2024 04:27:28 GMT  
		Size: 5.0 MB (4956182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:522cb35e375baa0f13eeb2b047a7967548e72504c16f270c537d37cabcabf541`  
		Last Modified: Tue, 17 Sep 2024 04:27:28 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
