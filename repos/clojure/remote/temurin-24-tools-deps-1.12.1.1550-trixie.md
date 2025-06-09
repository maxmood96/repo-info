## `clojure:temurin-24-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:02ab0cfb44f3f4dfb4a2644545f367a9904f4fbcebcb91e2655112955b953aa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:370547cfcf1ede9c80795f5199802531fe44677c8042905a925a2b71309c22e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.4 MB (227406605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd5f1ea2200ee267513a0ae844612674ea2486dcbdca94c368e10d60f1e2474`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
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
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca8130b01352467a2ae4563900dc69157eb0e08a50ec3d6fd6f3709b99e4feb`  
		Last Modified: Mon, 09 Jun 2025 17:19:37 GMT  
		Size: 90.0 MB (89951996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81afbd51f467babee0500e9ba761ffaced1edab50d9192847ee8406e980883cd`  
		Last Modified: Mon, 09 Jun 2025 17:19:37 GMT  
		Size: 88.2 MB (88206660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a1f6104780873b0c284e824e3aec11bec89219e98c3d295cd1b1e31a76d9b84`  
		Last Modified: Mon, 09 Jun 2025 17:19:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e59bc4b56d1a37e4e9599b276c60838db2eb2f6959fcc8b0f5a53db98abe2`  
		Last Modified: Mon, 09 Jun 2025 17:19:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4357a6bb8292e733810ba2d60b3521ec7c6a471fee0e5d5ae2c55bac3849754c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7425070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3823c9a48870bbe527ec61e77aa0cce736385ef480f16ba39c87a5611521d9ac`

```dockerfile
```

-	Layers:
	-	`sha256:8b1001c50474155b62c95f85437fb294965667469b18b7bbdd842661b8715201`  
		Last Modified: Mon, 09 Jun 2025 18:41:53 GMT  
		Size: 7.4 MB (7409281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5facc91781a4d2750f17b80d73b8e9861481cdd040000186b2cb6f45244596`  
		Last Modified: Mon, 09 Jun 2025 18:41:54 GMT  
		Size: 15.8 KB (15789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:70a8ea6019ac4c0b8a65dc30ca6284892eb52cf210c1a85622565c5ceabd5bf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.2 MB (227221551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9003b4d7921da7e1179ad079fb4c890dc8c1e6444d21a986dd7cb1bbc31e9365`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1747699200'
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
	-	`sha256:397826b9fe635f12caff1a603eb12c37426a5b3dc563e0adff2debff0c68a6b0`  
		Last Modified: Tue, 03 Jun 2025 13:47:15 GMT  
		Size: 49.6 MB (49618294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d7537e79c58dbcab2941c040399879be549690329edde2c0c79c2f4b2c6e312`  
		Last Modified: Fri, 06 Jun 2025 12:15:10 GMT  
		Size: 89.1 MB (89091276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bba0313948318694bf2e813b0a4c677623c80a6a08f37ee813606b178bc6c3b`  
		Last Modified: Mon, 09 Jun 2025 19:18:31 GMT  
		Size: 88.5 MB (88510941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f097a649b6fedd5ef5bd7c36fd07163d0cb683153293721a1b00b10d01b5b3cc`  
		Last Modified: Mon, 09 Jun 2025 18:02:36 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5124a732a3de50007a3cf1b7ed2005bcc153480b46930ded5ed06625c908bf`  
		Last Modified: Mon, 09 Jun 2025 18:02:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b287e421f6527cca22fcea0e3f27f57f38299cd530aec1c6ba53c8abe7fe6b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7432216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d4cba4901a6bf2344770f14526f82121270aaad990d53b30a149f079659b84`

```dockerfile
```

-	Layers:
	-	`sha256:23cb42bdc33fd8c6213f72b59c698f035f26a86b5e8d2947822c1b69763c4001`  
		Last Modified: Mon, 09 Jun 2025 18:42:00 GMT  
		Size: 7.4 MB (7416308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abb7ef354673e9077b32cb6867db2068dbffb5b846975a3b443819e250ddbfef`  
		Last Modified: Mon, 09 Jun 2025 18:42:01 GMT  
		Size: 15.9 KB (15908 bytes)  
		MIME: application/vnd.in-toto+json
