## `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:ab98592ff73aef166556db07deeadab333cf711076782ef4f064a973315e9567
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:234e90e524c3df74e27a2804519162d59e6ac7bd102afa007459cb2a54976df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269969471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb22f9c8b3fbd774808f2a6a7fa5ab0e0b168c6c85b3fb49b3bf517c5acc0177`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 22:30:56 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 04 Sep 2024 22:30:57 GMT
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
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4568a53831465e25dbd054abf778e43fc38bf556079064603fa53fed825e741`  
		Last Modified: Fri, 06 Sep 2024 20:58:19 GMT  
		Size: 145.6 MB (145550098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:145a35787bdfe8a0355947d82f402c840e436ed98148211a04913c75da9c2dba`  
		Last Modified: Fri, 06 Sep 2024 20:58:39 GMT  
		Size: 69.3 MB (69337397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f87bba403892c0a8875ed74975fd48348ca93200c61090b71947af659e36dac`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3c7cb0b243453e4b70417e561cb0b7eea9c17c98a94ad49c32b1b4d87e2e2f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7054209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c414492f58fc91b9f53b1f1028d95c24fa3929bde742ebc7c3d8ce0b3f54e0`

```dockerfile
```

-	Layers:
	-	`sha256:6a6cb2742c15a1ba5f399988f26b5403beef9438d911eafbaad2d0a7cd1a8e5c`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 7.0 MB (7040344 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69beee7d3e6540f68778a91dae347835723c1a319cd11379b63ab9f707151672`  
		Last Modified: Fri, 06 Sep 2024 20:58:38 GMT  
		Size: 13.9 KB (13865 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:eb0c283917210c04a15227564ee1a46f57909db6b7fb4e87db673a1923f50586
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.6 MB (265553700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aaa7254c2ce26cae2b0f29a203a71d97e5175112eb707e406fc049dda6ebba`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 04 Sep 2024 21:39:59 GMT
ADD file:aad8b86b3a958bc07504985acedcc819faa4f1ed12ca8b46d8d94c4d564cbdfa in / 
# Wed, 04 Sep 2024 21:40:00 GMT
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
	-	`sha256:d82c4492ee91810a42e0c53e955a661e9a092364bc474c9db559ea5b24b7047f`  
		Last Modified: Wed, 04 Sep 2024 21:42:52 GMT  
		Size: 53.7 MB (53731619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cf2c09432ac53db7f26275a2f1acfe047e96b9c7e794821debae994f169af1`  
		Last Modified: Fri, 06 Sep 2024 21:12:06 GMT  
		Size: 142.4 MB (142354821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5c96ad90dda4f5a108001bd421133c3d810268e530abbd3d0bf43dbf07772f`  
		Last Modified: Fri, 06 Sep 2024 21:16:46 GMT  
		Size: 69.5 MB (69466613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60afa175989384d7650f0db5a2274985df8af7d0384fb7f9f3278d04340f1a3b`  
		Last Modified: Fri, 06 Sep 2024 21:16:45 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2a9e6b8ed4d613c0978402927affcf8ec309c96f78a4ffe94ddecd3eac5ddbef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7060465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6a0f9ebdbf50db476504d843af02fdb3fc60a6e553bf26d8de2bc748d4c6846`

```dockerfile
```

-	Layers:
	-	`sha256:1c9298fcf65533c554d87006e9d84d0b3819171bfc29e2e54390ad87df20c21d`  
		Last Modified: Fri, 06 Sep 2024 21:16:45 GMT  
		Size: 7.0 MB (7046066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36a2424045a692750e9249499490107788a495eabb2b4e2356299f2994ae40a`  
		Last Modified: Fri, 06 Sep 2024 21:16:45 GMT  
		Size: 14.4 KB (14399 bytes)  
		MIME: application/vnd.in-toto+json
