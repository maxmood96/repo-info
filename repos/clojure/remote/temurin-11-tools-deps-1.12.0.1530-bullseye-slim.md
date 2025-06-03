## `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:4a506fcd9e03dc3fce6b22c9045bac465d6a2378d4c6f3d41df3d3fbcefbda1b
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
		Last Modified: Tue, 03 Jun 2025 13:30:16 GMT  
		Size: 30.3 MB (30255940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5435adb4c054b5edf3d6776553a009a610f56ed44dc0a40c3262662c9eee967c`  
		Last Modified: Tue, 03 Jun 2025 14:03:19 GMT  
		Size: 145.6 MB (145635638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cfdbe5acf332dd076585e8788d8642136ce742970937aeb0ae914ceaa59f253`  
		Last Modified: Tue, 03 Jun 2025 14:03:11 GMT  
		Size: 59.0 MB (58994187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f842c64b543be1198731ef212f54584d1e5a15417368b55def029665336456ab`  
		Last Modified: Tue, 03 Jun 2025 14:03:06 GMT  
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
$ docker pull clojure@sha256:8227ca8860c782d478d5e0c013f9270bf453d7219001ce0ad6014db01b4a70b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.3 MB (230296518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e6082b139902a8c837d7374953a49bbb89dcef0f0d9e178e81e572d18ab554f`
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
		Last Modified: Tue, 03 Jun 2025 13:30:45 GMT  
		Size: 28.7 MB (28746257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c7e75dcf364b2ceee07e82338697627a9716867e83933b2f790e9d0962da2`  
		Last Modified: Tue, 03 Jun 2025 13:34:30 GMT  
		Size: 142.4 MB (142420666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19addcfda4ed241500ea813d52c0b015d63a9d3f6957d1dcb0502e3556b9e8b3`  
		Last Modified: Tue, 03 Jun 2025 10:48:46 GMT  
		Size: 59.1 MB (59128950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52123b67cbe1e691a3f023962f14d3817df4fe9b70784a5c59f9371c7c32bbcf`  
		Last Modified: Tue, 03 Jun 2025 10:48:44 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b914a130f3f18bc04c3c3526b737b9ad5ce4a54f243ee2134c35b198be670938
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9100352dc878dc743bf62d60c9ac4d76bcfb163b04e04af770a1c122941826ad`

```dockerfile
```

-	Layers:
	-	`sha256:0962d404f18c27eec277ccd1af9561f04265bee9845ed1d577c69d0bc137328e`  
		Last Modified: Tue, 03 Jun 2025 10:48:45 GMT  
		Size: 5.2 MB (5195077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6eb113b517a95fd9ba7a8c7716bd53a61c63895fd9152beb4a7d4da62761fde8`  
		Last Modified: Tue, 03 Jun 2025 10:48:44 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
