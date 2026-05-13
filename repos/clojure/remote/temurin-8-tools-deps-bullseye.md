## `clojure:temurin-8-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:4145f54cd6088a6e9edc7110c19519ba57c59c9f7ee202a84615526f4f5c7399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ed730dc79473dc94dbb7811d72a8721c59dde552d52853a564a7a737d1238e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178560519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc3dab75506eeb1f0a52caf9af5f42da3bd5396c59bfdbd95ee1dfbbd9aeeee`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Tue, 12 May 2026 21:46:00 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:00 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:00 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:00 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:13 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:13 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4912797e8e728749044f9e8390a0ef5cc4b9073a6c619fb61713614977ef69f`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 55.2 MB (55198684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843c082a0c36f13b3e62f691229177cad5316612f2d86e316fa73b4e93e6e5ec`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 69.6 MB (69597846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d47fa1b243f93b669ac0eaa648a702f87bee6ceebd9eebbd1b2a2214e4691d06`  
		Last Modified: Tue, 12 May 2026 21:46:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:901c4db23fb80f26cbbe8f1f99804ccbeee452411cd3ab65d39147df581ccdc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817dd7abc20b7fa9f09e75ee5b8cac83272376ff334ae1863b737ca91811dd96`

```dockerfile
```

-	Layers:
	-	`sha256:cfccc347504f59b7f7a0a6b756132a0bcc20a0d75904cc463f13b2b5708ef6c3`  
		Last Modified: Tue, 12 May 2026 21:46:29 GMT  
		Size: 7.5 MB (7528640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:880053d081bb000f2bae4097efed2f7f4db56106b7a859793dd5efed491d5bad`  
		Last Modified: Tue, 12 May 2026 21:46:29 GMT  
		Size: 14.3 KB (14348 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:25c8af21c538b159edd5980413305e9909f5e30f2626e6d8f5106f2f6fcd6fb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.3 MB (176265816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0184b33e9b31985efc88ca0d844855cd80508fc5646bc524970695068438f0c`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Tue, 12 May 2026 21:45:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:50 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:50 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf00da27f15507125f10a19d7904b867d26b8afa19c4c98141b8b8d0b2668e3`  
		Last Modified: Tue, 12 May 2026 21:46:22 GMT  
		Size: 54.3 MB (54272926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acaf9d949a257462d888e8fd06146289d4b10ce073cc3bc6379dd43d79385288`  
		Last Modified: Tue, 12 May 2026 21:46:23 GMT  
		Size: 69.7 MB (69739032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9beec753f76ef2230330c07eb8c5677b5c7686eef7fd59f969071f540e7964b`  
		Last Modified: Tue, 12 May 2026 21:46:20 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0391f20c0a6c8352613e9de5d1267c62920c02c2a2340aad9b45ca622aa72231
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf1cd218af45d9471e59ee53dd905e7a1f2fbc7f533e31e92582faae6d5334bf`

```dockerfile
```

-	Layers:
	-	`sha256:62543bb7935c2222b5213232aa734af95bbc017da4bc3edd8625999c6019c12d`  
		Last Modified: Tue, 12 May 2026 21:46:20 GMT  
		Size: 7.5 MB (7534439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:859c52a2f7499ddb540a815e3d1774c3bca367f1ad53f864ec6b7e105a6fca52`  
		Last Modified: Tue, 12 May 2026 21:46:19 GMT  
		Size: 14.5 KB (14466 bytes)  
		MIME: application/vnd.in-toto+json
