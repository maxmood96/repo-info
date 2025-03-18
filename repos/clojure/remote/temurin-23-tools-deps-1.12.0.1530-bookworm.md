## `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm`

```console
$ docker pull clojure@sha256:b12e25c2536ad6a81b32109933cc9ec40cf449e349d760cc8a1f45ba3bb02661
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:f136c1cd140d1261000b9d8dcbf08a55686a4a1c88d76605ad58e1a5d85182f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294779204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d06f13b411c6ef2ab22ffccd396ce17af73cb154ba2819cffd3b5112c0f5e130`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ac50c17c4cc16a116ff8413d5f0b3d76dbf384045524bab3d1ddd0f6625e60`  
		Last Modified: Mon, 17 Mar 2025 23:22:00 GMT  
		Size: 165.3 MB (165316229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8b0bf0ec27c0bbce41f4588098fef3dcbd748f60525676eed1c862304f9fbf`  
		Last Modified: Mon, 17 Mar 2025 23:21:59 GMT  
		Size: 81.0 MB (80994095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c125b110c39c3086f68e50fb1711c1877c6c30cb94b8d0b18e8c8b1441d6d8`  
		Last Modified: Mon, 17 Mar 2025 23:21:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277512154e0c9c211c1d998e6288fe3a11c924a309e58de992eb6f296fd27b6f`  
		Last Modified: Mon, 17 Mar 2025 23:21:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ce154700fd5ecbedf27edd7d69939c8cb3221772e379c1c5acfb23e98345fd8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01157f037906d38bd605113bcfe5d4de4bdf63e17aa2e9d64bbafb8f49cce84d`

```dockerfile
```

-	Layers:
	-	`sha256:07fa2a5b154458ae59bf1242c7ff377a458740ae4d19f86709c2fc461766305a`  
		Last Modified: Mon, 17 Mar 2025 23:21:58 GMT  
		Size: 7.2 MB (7176797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:014567ac52410e54254d9bd488357d2934f535251f2c92393c20499e79945cac`  
		Last Modified: Mon, 17 Mar 2025 23:21:58 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6d1504b00ae2b8a63b2fde6a2d5c2961ae27ce0d284232c3dcc8426eafa095aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.5 MB (292489581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76d1eba205423611b209a89400a52b17919efc4cbf66aaa3fadc327d5dacbe4e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 08 Mar 2025 19:45:48 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Sat, 08 Mar 2025 19:45:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Mar 2025 19:45:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Mar 2025 19:45:48 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Sat, 08 Mar 2025 19:45:48 GMT
WORKDIR /tmp
# Sat, 08 Mar 2025 19:45:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Mar 2025 19:45:48 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Mar 2025 19:45:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:545aa82ec479fb0ff3a196141d43d14e5ab1bd1098048223bfd21e505b70581f`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.3 MB (48304855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9ee6b4c6e97f4c56459f18b4913e64ce06bc37df30ad27924127aeff6d0bf`  
		Last Modified: Mon, 17 Mar 2025 23:42:32 GMT  
		Size: 163.3 MB (163341415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f709858ef65b23c7d5737be38909e71fc58de81431ebb99cbc51b95ff715e1f7`  
		Last Modified: Mon, 17 Mar 2025 23:42:31 GMT  
		Size: 80.8 MB (80842269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaff36465c688e757368cd3fa82be1d99790b14a6bd58bac485b71ced1d31b49`  
		Last Modified: Mon, 17 Mar 2025 23:42:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c1ab1192c466194c927d77383d3c582d0f72f7ef2f32e1f74d4f85efb2dd5a`  
		Last Modified: Mon, 17 Mar 2025 23:42:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-1.12.0.1530-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:b1cf31522e46940418cd0cb4fdfe8fd234ec4bedb80f5203b66e7f9562a2f1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7198609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c9785d7a22858a702b1b72b0df3667f1fe32ea86d6c534f2e56859ff527db43`

```dockerfile
```

-	Layers:
	-	`sha256:8d666100a136008d1ecbb98d4fafe104d7676d34456b60ffa4ea7195543d7abc`  
		Last Modified: Mon, 17 Mar 2025 23:42:29 GMT  
		Size: 7.2 MB (7181963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6c52bf9a650f73a7af69fc226a4fdbceebedcd30e9dfd00fa262b864cc810f6`  
		Last Modified: Mon, 17 Mar 2025 23:42:28 GMT  
		Size: 16.6 KB (16646 bytes)  
		MIME: application/vnd.in-toto+json
