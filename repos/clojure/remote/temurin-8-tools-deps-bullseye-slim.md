## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:0d723e868aa6f462e0d51fc95a7af6083c4c29e0d0892d1a06ba5278ec087ddb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4d06a7c35ffb1ff8ba1c8da7c699fd36257771c7b0d226c047c68ee8a683379e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143966855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:715b5ecca4c4a3e71744b0ab5c8ffae1675a5ee9ee18135da6cf186764087126`
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
	-	`sha256:903cd755cffc34ca73762e36994a0e64c1300a5fff34da8aa47ec6d208858465`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 54.7 MB (54716179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad5bcfa92e8a363e721a2aa2ea8bf5c0eac43eda8e5414dc3a7c0f8db629e96`  
		Last Modified: Tue, 03 Jun 2025 05:15:23 GMT  
		Size: 59.0 MB (58994091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b4e35df37660a10563ff471cf05b03702e7f9217dbebfba8a84d5e87842a37`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:907eac6d4d8501c5df35bdd7b2b53c1c631261ddc7798c69563c7cdfd01bdbd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5304487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f30a020397f9d977b0fa82a4e2324225ca24d0ec1a3da97a3a6161ec6540cdc`

```dockerfile
```

-	Layers:
	-	`sha256:4304f960ce34526a8c89ce34a2592e0e6cb87222758db0fd2333e0366d25cfbc`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 5.3 MB (5290196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b718bc66edf4306154c73a7cbcbd5333df26288283e96f7f9a307d7caecc0ea`  
		Last Modified: Tue, 03 Jun 2025 05:15:22 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

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

### `clojure:temurin-8-tools-deps-bullseye-slim` - unknown; unknown

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
