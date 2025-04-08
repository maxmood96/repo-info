## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:0566f1a93daf480212433ed2feca71798d36d3921a836b629fd7c714e3918c62
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:085ca9cdcef090e945aef06a8c04d17ea9d61331b4a9fa96c15002a328d6772e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177865495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72291fd37d5fe4714480b54cd3443916c42ef800668f31d3b0d03803f41298fb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db53c705a9d628ac6757c867a624798248461802b072781bb9075866143d24f3`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 54.7 MB (54721234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e34ec775858a8f91ea0c465394df60dab0dfe9e26a646bddbef494ed9fd42e7f`  
		Last Modified: Tue, 08 Apr 2025 01:35:21 GMT  
		Size: 69.4 MB (69395088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659be8ba725808debe79521bdfdef6cdafe241c30c49872db333218f12d4a182`  
		Last Modified: Tue, 08 Apr 2025 01:35:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b225fa0219e08cf72bfe0f0852752202c7847805ec23b1dc76cf44916fb387c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05bdf6f55bc95326d900c79c493f2cbde3a9d0f3e2d12151f25bd3ea2b0f5f9d`

```dockerfile
```

-	Layers:
	-	`sha256:3daf333b36d69375853b31b12d3dc9e41bb17b1b8a46d7cc3333611e3ddb8116`  
		Last Modified: Tue, 08 Apr 2025 01:35:20 GMT  
		Size: 7.3 MB (7328111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1eba766f76fa64c8b5a9dc62ce8dbbf87d49124d74cfb2b1355be3b439a1ab9a`  
		Last Modified: Tue, 08 Apr 2025 01:35:20 GMT  
		Size: 14.2 KB (14237 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:210cc4e7d052b44168fe7942796bc98f8061064783e487085c063800e6b0f199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.4 MB (175377688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bdba13dbb89fbc6452b8a9d8d293c3bdfbe631f5a7e5bc1d0ead8a5e5df3f3`
-	Default Command: `["clj"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:7d61d9dafd0c900d9eaa97f9411b10213d45699b9afb91aee676649c07fc4a51`  
		Last Modified: Mon, 17 Mar 2025 22:18:23 GMT  
		Size: 52.2 MB (52248394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6eaaf3ebe4ba68f1eb575b9279af015ebd45b24b1a550f4f430cd4606a68fc`  
		Last Modified: Tue, 18 Mar 2025 00:17:44 GMT  
		Size: 53.8 MB (53822778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2935577889e729a550f7d714c82c8177cb7be1a1abeaf3b7b25752170f8e785b`  
		Last Modified: Tue, 18 Mar 2025 00:18:28 GMT  
		Size: 69.3 MB (69305871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33afd3a71ee71b7b946dd4ff884a7492a963d34c1eb247858c2a942a8c68ebce`  
		Last Modified: Tue, 18 Mar 2025 00:18:25 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:b212c646de918428cf0ca1c96b56faa0667802e1db8e186a0a93a9af5adb5a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4099dc467f070c2f1ad52ded27e31c3a8f204c30124273648af3f4a83b05f69`

```dockerfile
```

-	Layers:
	-	`sha256:019f6756fab4f2bc4bc0604743a62b2ed91d67103a7d510663ceef253a45770f`  
		Last Modified: Tue, 18 Mar 2025 00:18:26 GMT  
		Size: 7.3 MB (7331962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a6f5600c3f618c3bfa40bc7672309ddf1973c6db0a96ff2e212ba8e599f974a`  
		Last Modified: Tue, 18 Mar 2025 00:18:25 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
