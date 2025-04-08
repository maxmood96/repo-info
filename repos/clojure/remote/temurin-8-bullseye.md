## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:8fd7b5596621e530da813faa208334d8892710b47c17ee5174928958c437129c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

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

### `clojure:temurin-8-bullseye` - unknown; unknown

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

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6ce693030f10ad81cc99d2b3a1e354bceb16ba4021dbfbbaab43e81a24444e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.6 MB (175607330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32db50f687c6a9acfcd0f07db8db62301a18eff650f18792964a0a5845a5541e`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
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
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011f43d9c7f160c22108fa13dadb65f3cd9650c31975bd0819a245562f20ddf4`  
		Last Modified: Tue, 08 Apr 2025 11:13:59 GMT  
		Size: 53.8 MB (53822752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75204885d39245788315b592e08abca3ebd024ef73f61815cc83d376710808f`  
		Last Modified: Tue, 08 Apr 2025 11:17:42 GMT  
		Size: 69.5 MB (69529711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c88932de12fecab025c7ac33c8b72781ed2d9e34f29c852b6ba2ab268320621`  
		Last Modified: Tue, 08 Apr 2025 11:17:40 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:cbe90075722f9b85bf77ff8697bfbf490cc6d01c26ed43d847311a6c26fa1637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7348263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffe83dd56f46d13fcb088760d76fadd66f5444c277492dd01d099b464a57e80a`

```dockerfile
```

-	Layers:
	-	`sha256:9dc5aa87284d3834af8d1ce9e313e9874446c2b2e854d0760ad4583c5a19d62e`  
		Last Modified: Tue, 08 Apr 2025 11:17:41 GMT  
		Size: 7.3 MB (7333908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d80f140e1f48ab1ef43a2ca9fc82d77aed4ee7338953a6ee74a6ea0da74384cb`  
		Last Modified: Tue, 08 Apr 2025 11:17:40 GMT  
		Size: 14.4 KB (14355 bytes)  
		MIME: application/vnd.in-toto+json
