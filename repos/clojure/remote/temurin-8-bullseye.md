## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:0cb677b45502df627bf336003c4f086a72b119041d01659ed362480f8d34fdef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:f22daf7e0cb388fb75e10ef29a48ecaa7dde8312f14575185a135204f0737a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177865110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60e2caab2f2d13bbe248e631e27c8e0cae9a1906f5b05f938f0eead4374ca26`
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
	-	`sha256:7c9caa446d6bb2207a2f85b620687c9451ad4299d7ace6427e233ba4cd566998`  
		Last Modified: Wed, 09 Apr 2025 02:18:17 GMT  
		Size: 54.7 MB (54721225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af7fced4cb913ce4885d1672ed9bfd732e44ec9309068afbc07d1b0836785005`  
		Last Modified: Wed, 09 Apr 2025 02:18:18 GMT  
		Size: 69.4 MB (69394708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a70f018095522da05a9962332bbd96669ea6537cfe75325222ae87405a96f`  
		Last Modified: Wed, 09 Apr 2025 02:18:15 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:be3a34938968e4cc4a6aba050fb87555c29db46ccd7ff78b33a0bf777461fdf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f07723a134bb56a4b223298ba280d0806a97f6899b0f4a1c765f671c92a97ff4`

```dockerfile
```

-	Layers:
	-	`sha256:bbccfc63b008a3952f273fab42568a25c0d95ca2a9e292c37efb37031121e01b`  
		Last Modified: Wed, 09 Apr 2025 02:18:15 GMT  
		Size: 7.3 MB (7328111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7b1b1e326132570f991d1daa6a9722380560b7420851163563ec24612d5be24`  
		Last Modified: Wed, 09 Apr 2025 02:18:14 GMT  
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
