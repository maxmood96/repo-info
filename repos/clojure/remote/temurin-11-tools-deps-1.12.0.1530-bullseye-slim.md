## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:f5b7bc30312fc630f0c86d3ffdca1ec1a84ba0721cb44d1da8c484a5067be99a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:cb39cdec27f6cb8a72bd376d7b54538d00bae21cfe9c973ce8cfda7b279828e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.9 MB (234886409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:766324357263a5c042c354f8f3958db97161b31f22d75734ab8969edc08ea674`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:e1f16b66c2e86ad38458eba597e4ec79e4750398a28dbbc2d7819d829c4c9023`  
		Last Modified: Wed, 21 May 2025 22:28:05 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435adb4c054b5edf3d6776553a009a610f56ed44dc0a40c3262662c9eee967c`  
		Last Modified: Tue, 03 Jun 2025 05:16:05 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdbe5acf332dd076585e8788d8642136ce742970937aeb0ae914ceaa59f253`  
		Last Modified: Tue, 03 Jun 2025 05:16:04 GMT  
		Size: 59.0 MB (58994187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f842c64b543be1198731ef212f54584d1e5a15417368b55def029665336456ab`  
		Last Modified: Tue, 03 Jun 2025 05:16:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9036e86fa8ed5a36d3037bfd9b1e5e65edf8d8072e9bc73e3505b615c48991ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf4531e675d06d4d2da673c0e82a9d5d4e85bb47f754ce239f8b1975b56755d`

```dockerfile
```

-	Layers:
	-	`sha256:16511371d3093122b15dc35c10e7be84e5d2038e058509dc8d716c7dfe4a167f`  
		Last Modified: Tue, 03 Jun 2025 05:16:02 GMT  
		Size: 5.2 MB (5188727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:138d66e73a5d2fce09aa8520ab073afad86a60382a37af0d42c141c10d9489be`  
		Last Modified: Tue, 03 Jun 2025 05:16:01 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3c5cdc51504ab685ec9f2d86b0af18617298458126e94bd45d4c9eb5be28567a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230296663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c713c38f8b6c1fe4eef97da34ed9f7733cec5e1e34a8cb5f15e579c3f72dcb0`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:66850c8b65c1e9c3674a722b71f8887dd317a9b257148bb1063e88d85790544f`  
		Last Modified: Wed, 21 May 2025 22:28:28 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4089ffb1a4dff6639b70fa34d83a369967ffca2c451e73ba59edfdf735eb232b`  
		Last Modified: Thu, 22 May 2025 03:17:39 GMT  
		Size: 142.4 MB (142420720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ae7b68c1876f8d0c354fbea2536f9d8ea7c42c37a9222d5c50ae618b707891`  
		Last Modified: Thu, 22 May 2025 08:16:36 GMT  
		Size: 59.1 MB (59129041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfd493c5cf1997f3ec3b9b76d3765064435a3d494a284cde9a8447d6dde421a2`  
		Last Modified: Thu, 22 May 2025 08:16:34 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:35cc945163916b7c56ac49bf2ed039a0e3036f2a4943ad1bbb7039a8502bc1b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8512a04abb45963a48516911a508f222f5ddbc9de55610f4c5efc2b45f0ea2c`

```dockerfile
```

-	Layers:
	-	`sha256:05c06709d817427368ce3b0b26233487a908c4f4c74abfaceddaac4c9e29bd6b`  
		Last Modified: Thu, 22 May 2025 08:16:34 GMT  
		Size: 5.2 MB (5193481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c562b3e2eab01ea260ae8a4db365cd77745d4ec50cd9a0191962c1dd933ebe7b`  
		Last Modified: Thu, 22 May 2025 08:16:34 GMT  
		Size: 14.4 KB (14427 bytes)  
		MIME: application/vnd.in-toto+json
