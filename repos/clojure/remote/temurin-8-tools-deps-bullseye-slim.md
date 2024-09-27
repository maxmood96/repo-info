## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:a63fd9d0d1ef1ce37cf14af3281d06958bcb8e2f471475dcb248def7895fbba3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7714183680b0be7e929aecfff24147fd5f4ab6d097a146c07e2fd253a02f421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245869dcd429cfa7cebac57a64051722640dc4627f67a9fc54fff976dbcad2a1`
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
	-	`sha256:207c2ba6649b55962f49a9654e8eec555dd20620c00939c426a643b530a12fb5`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf82cc4305cad25f17887eeafb7211fecff533a0686015af65237e1b44521fa`  
		Last Modified: Fri, 27 Sep 2024 06:01:02 GMT  
		Size: 58.9 MB (58940079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626791723e83d46e4e149b93d892c7aab99bf657e63a1e7ac3882899e1b87260`  
		Last Modified: Fri, 27 Sep 2024 06:01:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8ef9f797d668db58378ae5d2db920c71411bb68a098d8a4ede6a0dab8f292e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423aadbd7426420207a19e816095486088ddc7f4f9ba0287ed473dc3cb867024`

```dockerfile
```

-	Layers:
	-	`sha256:02f2efa6689435394dd112d7a87e6f2cb55e40e7e5197809d82ee842e41f49d1`  
		Last Modified: Fri, 27 Sep 2024 06:01:02 GMT  
		Size: 5.2 MB (5221615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f15225f555f066fe71358a35b31ba814ca8bdd41ee6385aa186cb4fe674c242`  
		Last Modified: Fri, 27 Sep 2024 06:01:01 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:30c38fa92ac45e66ba3ef650626d2e7384377ab26191bead394c4d69914bb525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191876479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4c8c17d1715b45f6ea2728e04caba5d201569903e965c245c0c8b7488c0989`
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
	-	`sha256:6d15783766051f25dcae5628c7cab7446795e3ec78cfbb5df1d15887f5aef9b0`  
		Last Modified: Tue, 17 Sep 2024 04:10:47 GMT  
		Size: 102.7 MB (102729255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ef435c421bc233d75cc26e3935f220676601e40e5eeca3dfdc70c24d17f8ee`  
		Last Modified: Tue, 17 Sep 2024 04:15:42 GMT  
		Size: 59.1 MB (59072211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fac1b56e8ee0575ee44c831091e90d575a711419bd6438a7a87c1e658a578685`  
		Last Modified: Tue, 17 Sep 2024 04:15:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:907ff05fd80927e40c0b351f729558917f9d210db38829b66d2f18158abbc986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6f89b1081161873e8eed8fdf1844c64047d0a0daa3a64342c5261a3d78375a`

```dockerfile
```

-	Layers:
	-	`sha256:cd9e9c9a3c6463be08e1a99fcfba350e61d5c003d65143d240dc28f6d0023a18`  
		Last Modified: Tue, 17 Sep 2024 04:15:40 GMT  
		Size: 5.0 MB (4981673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05622050a9f366cf83910f7b480d71b51b74c74fbceb32a12bbdf7d598bd6012`  
		Last Modified: Tue, 17 Sep 2024 04:15:40 GMT  
		Size: 14.5 KB (14461 bytes)  
		MIME: application/vnd.in-toto+json
