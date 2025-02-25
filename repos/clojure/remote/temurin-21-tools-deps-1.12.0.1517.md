## `clojure:temurin-21-tools-deps-1.12.0.1517`

```console
$ docker pull clojure@sha256:60af2c348d2ba33c6f853c26b004a7806debb18254d07ec53489fccc70f1671a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1517` - linux; amd64

```console
$ docker pull clojure@sha256:9aaee686b9d4b79a2c0004909ca8662a3f0267a9cbee75dfcae64e93f5a2544f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287057409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bad43d4502f0ea789fb63d9346ab1326abf379247fefa9db3de47a93d1bc362`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:155ad54a8b2812a0ec559ff82c0c6f0f0dddb337a226b11879f09e15f67b69fc`  
		Last Modified: Tue, 25 Feb 2025 01:29:36 GMT  
		Size: 48.5 MB (48476100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ac55335407a6d8c8ffe607691aaca73b4317e1e3c5fccedea7670cbc6d07c78`  
		Last Modified: Tue, 25 Feb 2025 02:34:29 GMT  
		Size: 157.6 MB (157585882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ecadf41747f723a90cab99bd63fe50e3b60b8013af0697728bff714749dab7`  
		Last Modified: Tue, 25 Feb 2025 02:34:27 GMT  
		Size: 81.0 MB (80994388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473d24c23dcd27e9d9c1e1d219b205e9025ba51ff7afeb75a319dd7d44304486`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb02c65f51adfe5984be435a3e5c7aa14c13357249c35d7f180c28e18ffad10a`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1517` - unknown; unknown

```console
$ docker pull clojure@sha256:506146fc17cf27bf9f04b7e49df8047be1016b85f2c96433ce222663bbf83d19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7194019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a5d907c67ac0eea2a23068ec3d969826be2783ea57c9685c37c9627d37945a`

```dockerfile
```

-	Layers:
	-	`sha256:8479cc40f2990db2282e53702b424af24bec7916bd47069efb994b192d31fdea`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 7.2 MB (7176198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5ff687e66fbb5ea0533a86e1acf4c51029e34fabf32ef5a73a8563daff216b6`  
		Last Modified: Tue, 25 Feb 2025 02:34:26 GMT  
		Size: 17.8 KB (17821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.0.1517` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:971b25b737f17e4dd95863c6b6d56d7573b1f0aa241d0405d521832ed7b45d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285011597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f6e3aaf7f26607b7b990a41e3adf1fc0bd12232122338914f969339c32b4cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 19 Feb 2025 14:51:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 19 Feb 2025 14:51:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 19 Feb 2025 14:51:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Feb 2025 14:51:07 GMT
ENV CLOJURE_VERSION=1.12.0.1517
# Wed, 19 Feb 2025 14:51:07 GMT
WORKDIR /tmp
# Wed, 19 Feb 2025 14:51:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ba7f99d45e8620bef418119daca958cdce38933ec1b5e0f239987c1bc86c9376 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 19 Feb 2025 14:51:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 19 Feb 2025 14:51:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40336e7d22b324447830c219b494b909e6de502a901b046ecd7ac83cdf04cdb2`  
		Last Modified: Tue, 25 Feb 2025 10:48:57 GMT  
		Size: 155.9 MB (155859298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f2f687bce635a78ca4e3bd95906c8d14bff2061cba1ba5eb768cabcffd044a`  
		Last Modified: Tue, 25 Feb 2025 11:12:03 GMT  
		Size: 80.8 MB (80843250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a91297919a6bc4c894c4512056077913cefe4581550f5f127b8c92017ed7168b`  
		Last Modified: Tue, 25 Feb 2025 11:12:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2a0f345db0f3f65d294c12b7e31a033f9eadf8b8b47bdb8fbb6aa210855d0b`  
		Last Modified: Tue, 25 Feb 2025 11:12:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1517` - unknown; unknown

```console
$ docker pull clojure@sha256:05ef4e76f522c2771d81a39e736eb77af39572f95ed1dfbc6377be942f2316c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7200044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d5a9ac0ac258b56a5176fa3bf9ea3492c2d7dbf3cec9d9a5850fc3efd3eac9`

```dockerfile
```

-	Layers:
	-	`sha256:5d91582ed8eebb232a90465eec8d32fc26088e21607e91de80969e56ab740758`  
		Last Modified: Tue, 25 Feb 2025 11:12:01 GMT  
		Size: 7.2 MB (7182033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9eed95dc9b79b4f9d1db4846888f27aef284b5695593723d91185d5fd57dd0b`  
		Last Modified: Tue, 25 Feb 2025 11:12:00 GMT  
		Size: 18.0 KB (18011 bytes)  
		MIME: application/vnd.in-toto+json
