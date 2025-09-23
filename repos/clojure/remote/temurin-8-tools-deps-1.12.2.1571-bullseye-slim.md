## `clojure:temurin-8-tools-deps-1.12.2.1571-bullseye-slim`

```console
$ docker pull clojure@sha256:4b5df63da40ad2c2eea4ba60fdf23e89de18b7b3ed027274a6c2b02e3a1fd5ce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.2.1571-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ac8b2fcad17af5310f668d737a8695453c78d068a4f0ccdc012bdb02bbaf3ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144141760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97fa55800619bfae33c3c9ce78e24a534f83a0f72716ced09eeddc1215f1e55e`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:456a3213e1b1f193dc759cd05f6f8422428b8c4bd45ef40fbf41ba43bdce8570`  
		Last Modified: Mon, 08 Sep 2025 21:12:48 GMT  
		Size: 30.3 MB (30256068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2929b105f67a5d738799257c48c0c2607391426bf814223e405536c5a6db562`  
		Last Modified: Mon, 22 Sep 2025 23:44:12 GMT  
		Size: 54.7 MB (54731282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a31e96321e685a17022bcd50c5bf97f0bb7321a7252f62016a5daa411b62ae9`  
		Last Modified: Mon, 22 Sep 2025 23:44:11 GMT  
		Size: 59.2 MB (59153763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423a4072ecd1e6542c7152637838fc055295866c338d405fe03e10b136067b8a`  
		Last Modified: Mon, 22 Sep 2025 23:44:06 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d2d8e1eea8939d208acb97f1a0cc54565cce1ba129461b250d65c1b344c89b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5443968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:714cf7ba3aca95b0001dadf2c58e1ba037e8aa9676df0c3725f3b6610737b2d9`

```dockerfile
```

-	Layers:
	-	`sha256:8fb679ca18c2c46ae14b0480ec79d7466aff2045b9f4837b81c1cd769bb68fe5`  
		Last Modified: Tue, 23 Sep 2025 00:46:46 GMT  
		Size: 5.4 MB (5429677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6b2ffe4bcfd873a42c257d85da11eb1e944b59cfdfe474a5c1dae4ece79f631`  
		Last Modified: Tue, 23 Sep 2025 00:46:47 GMT  
		Size: 14.3 KB (14291 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.2.1571-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4c26e7622f0ff6cbfcd175e51128cc372bdba4b58a1ded65a24bc1cabf2b54d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141873958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61eea6b16a45c85cf13db7b63a938f7916c4d5b30ff5f6967715f98f64460185`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8568e9af3ab25a29d98aac9a07896467a19253e72e5be0cf09cd3982ac4444d0`  
		Last Modified: Mon, 08 Sep 2025 21:15:52 GMT  
		Size: 28.8 MB (28750457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0864b97473c5f9f6ff27fd8e3b13d152c9d0ae01ccfce2232697011ce00d96a`  
		Last Modified: Mon, 22 Sep 2025 22:16:25 GMT  
		Size: 53.8 MB (53835608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f089bb38a69bb664f64717ffae90aee5cd2bdecdafd8308a5ecc5feff98ac9`  
		Last Modified: Mon, 22 Sep 2025 22:16:26 GMT  
		Size: 59.3 MB (59287246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f7bfb50a186dd35c7bef6f22c753eeab02b9c6bdc3b690059379057c60c372`  
		Last Modified: Mon, 22 Sep 2025 22:16:21 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.2.1571-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:98c01b49589256275c5e8643cf4547eee9e68c57f7929488e4fb9017b3e803f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1090370fec895df13d21b3fec4a561281d82dbacaa072eec4040eb715c9d77c9`

```dockerfile
```

-	Layers:
	-	`sha256:3ff5f94ce370d8be4b91590ef0e63ff93a3ec37d466ac55fe11811db27c2850d`  
		Last Modified: Tue, 23 Sep 2025 00:46:52 GMT  
		Size: 5.4 MB (5436107 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73ca92df8b3b8352f19d71deee186819880d4308e31059037281b09d67d37b90`  
		Last Modified: Tue, 23 Sep 2025 00:46:53 GMT  
		Size: 14.4 KB (14409 bytes)  
		MIME: application/vnd.in-toto+json
