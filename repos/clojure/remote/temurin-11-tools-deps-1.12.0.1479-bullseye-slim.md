## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:e89e2655e8c2dfb2169e916900b350d8267bc47f96979bef13171b81af63d754
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

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

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:22ac58e46c64876c49e634b49e1d553b34d016ec612a4ea43a80f6771ef4eecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231503932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd57201d171ac953bbbd11295ae6a9f089c0e6a07fd90061b4f171b5fe6b53e0`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30149fff09dc33f83b6ab4318fbe4dd4f83df2dc3e54bf33b92b83879e58b67b`  
		Last Modified: Wed, 02 Oct 2024 02:12:34 GMT  
		Size: 142.4 MB (142354841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74861c9197d2d977035c28c9f32801184a03d7cc9b39e8d2055e080ad5c2663`  
		Last Modified: Wed, 02 Oct 2024 02:16:47 GMT  
		Size: 59.1 MB (59073290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a223ba140acd6ff0a2f3001cc493a9b651bd263c10ea0876d77220c8ad741ad`  
		Last Modified: Wed, 02 Oct 2024 02:16:45 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:874c1acb6530893aad62cd58339a34ead94d2684b1c16de9a7a6894b4db8f423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd378a6bb68443df072ac0398cf0474f7b581e0ef44c6157e2e671883aeb82d`

```dockerfile
```

-	Layers:
	-	`sha256:70c126221b921f1877d7704a767a672ee064ddcd12d1db71c1e3a48016388824`  
		Last Modified: Wed, 02 Oct 2024 02:16:46 GMT  
		Size: 5.1 MB (5126008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df4d40e0ef83ea603c1f76134ca8ed550f3b96dd58fe90340d44b2d03fd0508`  
		Last Modified: Wed, 02 Oct 2024 02:16:45 GMT  
		Size: 14.0 KB (14049 bytes)  
		MIME: application/vnd.in-toto+json
