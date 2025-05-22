## `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim`

```console
$ docker pull clojure@sha256:67ec248874de3c75dea8ced4e355033bda80b9ea6b0872d1bd58692589abd793
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7e47ccb43f9e3d98816c46bb01bd33f3cc792a9cd5e100ab60de4f3367f4a9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143966743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:906180469cd908e551d00d368352ecc0f08d86126efa6bfc5e484b3cca84422c`
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
	-	`sha256:efbe380a355495bc5e38d6d1e3e5fec428c3fd1273c709246bd8ce0d0fe64254`  
		Last Modified: Wed, 21 May 2025 23:31:54 GMT  
		Size: 54.7 MB (54716171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786df985e83238a21611bd54d4945ce34614be77183910f49549af67930ab940`  
		Last Modified: Wed, 21 May 2025 23:31:54 GMT  
		Size: 59.0 MB (58993988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137049063f3183a0773f866481facfd67ce0c1b01be4a10fa42683dc0a031929`  
		Last Modified: Wed, 21 May 2025 23:31:53 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:3add01800cda1ff37e4987807ff874fbaccf5c121edaaf5870d716f1c93f1fd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5302891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a832c9016bdb134373e05e8df52efd6fbe7de9727f5f06dc6e418c1e6e5f08ad`

```dockerfile
```

-	Layers:
	-	`sha256:8d79f112c6144f70bd185824daec86f8ef876b74394d942832d9b6fc67f27022`  
		Last Modified: Wed, 21 May 2025 23:31:53 GMT  
		Size: 5.3 MB (5288600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ae5ec3172aea3fea7276a64c6d1d9739f28a651587df381f53c05fbd576cef7`  
		Last Modified: Wed, 21 May 2025 23:31:53 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8fa4474b5524675077ef5898dada8c5bd4f67a7249fc44d8bb746ce7e46eb893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141706424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2cc501ce11f6bb48de91279d62556a7c7ab0772382977546663db4f6fbe667b`
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
	-	`sha256:3efe5d7855e772307b89e10a4ea2cf30996156bd1dece1d9fe7327ed1bfa72da`  
		Last Modified: Thu, 22 May 2025 08:02:36 GMT  
		Size: 53.8 MB (53830503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452b34139e90ca4ad1bd747c8e13be945a5afb1e279fcbcb3baeb3aae4c092e`  
		Last Modified: Thu, 22 May 2025 08:07:00 GMT  
		Size: 59.1 MB (59129019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1bc9342073d95135f80d4ece5f62ea361744e18575dce741108e0b8304f790`  
		Last Modified: Thu, 22 May 2025 08:06:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1530-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f9dc86486ca22cd2481bfe607dfe2e795a88a0347b8abd46765b030e3889afe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5309439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b878fda5c39deeddf713a8457944fac7ef8ce8d6782a46b406e94e1ece0bed2`

```dockerfile
```

-	Layers:
	-	`sha256:bd862c3e948879c643bd5d23321f9c3a37f6ed61038357f7e20e7d15739f8820`  
		Last Modified: Thu, 22 May 2025 08:06:59 GMT  
		Size: 5.3 MB (5295030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd59292fc376dd30a1857200d8e9199168c4d20c203a0dbab1ebcd6fdb82770`  
		Last Modified: Thu, 22 May 2025 08:06:58 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
