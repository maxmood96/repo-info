## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:8f99de03e0ac68ee4279ffed13de87132506006ad2954c6e5d20260a0c7d1ad8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ae8dd759dbc8be371391079689a20d5c1c21ed73309a2dff2bfd8a9d17716e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192643294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c347679ef24a9e538a8c9636059a2ce1cddd53ce835654a15c6e8953cda1c642`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:6c87eefc1f428634061bcdc9ec95ccceecd7c7475d35a777479af83f64ee6915`  
		Last Modified: Tue, 24 Dec 2024 21:32:32 GMT  
		Size: 30.3 MB (30252643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d43847c8e4a95a5905b22ce29a2b2670b6ddb2002f50f0c8b5b3eb79c8e70ac`  
		Last Modified: Tue, 24 Dec 2024 22:37:28 GMT  
		Size: 103.6 MB (103633884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8398e583aad7e32c781346280b3b589b95e18bba78897f41f2701f5daeab59f7`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 58.8 MB (58756122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75f5c6c4a5c8cae82314108a37915401aa9cfe066c6b6e9ba6ffc7791d8a6678`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:439539bd3a4685fb8739defcbc5c8316d5ca375f390eea58852660429ea08bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00954710659e6e577068e8292c4dac416d5f2f724596c9a34fa8f75097eaeb0c`

```dockerfile
```

-	Layers:
	-	`sha256:5fff89bc0e8cde6679f8591fd01279ad78718b12ca6b86c8189199588541ed7b`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 5.2 MB (5239225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d21d6eca60b99207e87a85fcb92777c1bbdd98cd8b2af198dbb41c12581be37d`  
		Last Modified: Tue, 24 Dec 2024 22:37:27 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:77bff8e8fc5ba93c512c046364eb3b465cf2d2f8fcbbb079c7e23aa642bf5fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.4 MB (190373616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2affe06c124a2ddcf308067d180a424c2544fce1440bd6ac719568404289fc72`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5004855b7bb2c7db6bc64471c5e9b9b7737ee2673220c268b8f5feb653a54e00`  
		Last Modified: Tue, 03 Dec 2024 15:03:58 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd367d6c5041d4b5b22261131e963f2350fb7c3f4fe3924357e0a20a7165e71`  
		Last Modified: Tue, 03 Dec 2024 15:07:48 GMT  
		Size: 58.9 MB (58880332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58373b123069ca5baa343c208c393c7a7c3d966abccb259f564c94be90ac290`  
		Last Modified: Tue, 03 Dec 2024 15:07:46 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fb19b0b236a99b7165c7a77fc48b0fa22059b48c1e960454de9e1d829b1bb0db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5266568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0728363da0852291aadf255575dfb333f1b1e1c538bcb1f16163498d7d3cd5bc`

```dockerfile
```

-	Layers:
	-	`sha256:4a979ab40e4563f5e465170b151aeda926346388647d51317b228e31939fa238`  
		Last Modified: Tue, 03 Dec 2024 15:07:47 GMT  
		Size: 5.3 MB (5252155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135b5392f0d759b7be0afb01671a6368436a2f3d23d46f012685a7dc8009073c`  
		Last Modified: Tue, 03 Dec 2024 15:07:46 GMT  
		Size: 14.4 KB (14413 bytes)  
		MIME: application/vnd.in-toto+json
