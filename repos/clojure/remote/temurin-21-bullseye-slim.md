## `clojure:temurin-21-bullseye-slim`

```console
$ docker pull clojure@sha256:ae3624f0349fcb43208ac783121bd1a47f142e46dfa1be97951f2f13f2fddd93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7749ffa75122345e205b3c2a288f0452fd0b3fdfab752eaa61489469e1e6e7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.9 MB (246897065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c122e20449f47aec2443a878c5a09ec21e9b06a6aa6dcd320a41b70884f5124`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff75de60eae0102b0443895c1c203f3fb4e005094fba361f395e68d8d7174414`  
		Last Modified: Mon, 09 Jun 2025 18:57:54 GMT  
		Size: 157.6 MB (157634504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af41d21ce9405962b168cb73209eb36a6847802876232ae9771e1ba686385ebb`  
		Last Modified: Mon, 09 Jun 2025 18:57:42 GMT  
		Size: 59.0 MB (59005577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e957925ad4b0e35400e92d39a87c9d22c623a508d1b90d620d881a582f73615e`  
		Last Modified: Mon, 09 Jun 2025 18:57:39 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3667cfaeb4d9b6657623e8941fd707b52ab79d95c8e4fb37ad1bdd75356da70b`  
		Last Modified: Mon, 09 Jun 2025 18:57:39 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9e369eeca9c6a9bbfcd7ea4bdb6ae7be8dce410af8bf9e56d8ec4b99896ac59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a77712019610d51c06ddae99bda2ccfc5e06b309926d4c4ca6381f423ae24a9`

```dockerfile
```

-	Layers:
	-	`sha256:c2e7a7e4fc316e7f8c6782a0478fdaa7bd9c7d8045d2e150a4006378a832fa1c`  
		Last Modified: Mon, 09 Jun 2025 18:39:18 GMT  
		Size: 5.3 MB (5313460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746f8cb942a864c4042771c491b495c71190ef015ae7a9d6c635c001826d173d`  
		Last Modified: Mon, 09 Jun 2025 18:39:18 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7e01b40eff1dd85f413783d8854c2ba104fd56b3512393defb3c73c23b62405d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243813644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b27fae55e006c8938cf7aa093048735095eaa4dd83e468f06856364e3809b4bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c27f9d6798235ccf5e5f695d350773cf03adc77fea3cfc1049c69b79bf7dba`  
		Last Modified: Tue, 03 Jun 2025 13:32:50 GMT  
		Size: 155.9 MB (155928816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e509e5d802592d3a169b1affd0865398fa5208ee51e028251723de71ab5a3cea`  
		Last Modified: Mon, 09 Jun 2025 17:54:26 GMT  
		Size: 59.1 MB (59137530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4eb5c12b2ba7fdc2b6c66313498f8f667aa90a3731813222738742c5ef4988`  
		Last Modified: Mon, 09 Jun 2025 17:54:21 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34feb0ecb046a3a2fb95b7973432735e02955500b27b74182b2c6c98753ae649`  
		Last Modified: Mon, 09 Jun 2025 17:54:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f2d60b55f117dadd1e01ffb58daa0b8cad914117018d3fb6d3d80df331331dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5335933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d464d634b1b40c6bca3eae9796a7b97273b3a97f846b0c79315675e73bce2ca`

```dockerfile
```

-	Layers:
	-	`sha256:7372cab2600b349299c4ade4c81514c981394fe613bb8b6d4e1956527db66078`  
		Last Modified: Mon, 09 Jun 2025 18:39:24 GMT  
		Size: 5.3 MB (5319216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2624ecfc40e6dc2b6afe8dbedd4b789fe9cfb2fc402363688f19bd980e5d9105`  
		Last Modified: Mon, 09 Jun 2025 18:39:25 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
