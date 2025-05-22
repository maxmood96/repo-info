## `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:6c572a61a1752f39ac212490c341113b6ec2bf21b6024d5733c9caf5fa63d908
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:936568a299d4a2b3e09a5dfa7486aaef49f1f0b4714f09d54dd67eddbfe1f3be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179203207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4cecb44a45718f331311143db7aa90e2ee5820f65a30e19543ee28cbc1e07d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b017c5e0640baf60ca49edc47354a0529a041cb95f6dfd2d805f3cf6fed6cfe`  
		Last Modified: Wed, 21 May 2025 23:33:53 GMT  
		Size: 90.0 MB (89952020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fee2dc06ca5d0260bf75a2472d7d0be4a8a757cbeb759b4c3f22388d8220fe4`  
		Last Modified: Wed, 21 May 2025 23:33:53 GMT  
		Size: 59.0 MB (58994208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82e69e98947cb2416a766f6f43da4e60d10db308da0bfd407cd84921caa93ab`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372a48543fe9526906ba2548ba73e5ad81d58a9b65b553ef9a7d9dc668b5c59c`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2b198cfcb95c09ab66c4cb0211435c90524fabb13a56d976b0469d8606d18a1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9da917bbbf050d89ab0acd0f7390bc66bb3ac3eb4603c31ceded05a6cfd28b1`

```dockerfile
```

-	Layers:
	-	`sha256:251d65cbea4429376f73c4cf559df5d5ce04dfc14a3e454d2f0b5479e8b0fab1`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 5.1 MB (5117636 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79eaabe616f6217e59e89b84649dbbea9b4c6b75ee1151a79f51cba2454c3214`  
		Last Modified: Wed, 21 May 2025 23:33:52 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9935749937754d3a2890b07f1b805043259eacb58d012d21436ba8192d8379a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.0 MB (176967506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9019c66c5100491330cb565b98c5018c1211ff1ea4e284335249f8b3c9ef02b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c230e87d938d3a9a7780c78743a419e4444e2d33614777a306afec58de57507`  
		Last Modified: Thu, 22 May 2025 08:41:20 GMT  
		Size: 89.1 MB (89091279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0715ca920298e04754e06b56fce69361eb14629e32104ac01b947a9ca967ac55`  
		Last Modified: Thu, 22 May 2025 08:46:05 GMT  
		Size: 59.1 MB (59128929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a105c53d3f758dd3a084d9a1febf46a95c28213daf3b411f429cd32eeda2fdf`  
		Last Modified: Thu, 22 May 2025 08:46:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6ea48c9b691285bb971d09153c314435fcee2a9fa4bbfc6d468c77a58dd615`  
		Last Modified: Thu, 22 May 2025 08:46:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9735961820c61e9b52120d59eb875c2152d42e070bb1161759078ad907e6e255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5139355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9164eda1793efc1ebf1858773acbd53223d59b7f6a91fdc0e127e7cc15c793cd`

```dockerfile
```

-	Layers:
	-	`sha256:0624b22eef4c75428ae77be2e44c3b3c64f980dfcfa96829d6b98c6610015981`  
		Last Modified: Thu, 22 May 2025 08:46:03 GMT  
		Size: 5.1 MB (5123365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:552fd3c1edf6d116c0484f307b8a66741758dc206f5a2155661976800f953eea`  
		Last Modified: Thu, 22 May 2025 08:46:03 GMT  
		Size: 16.0 KB (15990 bytes)  
		MIME: application/vnd.in-toto+json
