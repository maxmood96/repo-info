## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:32c32de24ad6229910e71a00520dc4a3c7bdb6dbd70c3fa7620503e8ab2abc45
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3c1f04334665229b23621c438b656c6625a77596ef64968f219e146177a767fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237176929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb27e29e485ecd8f763c671a59ebf58beac15f36493aeed61efaf973e1a9a31`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:655004cf4b175db2bcc273867245c753bee16ba55bae840ceb487c0e8bbec6b1`  
		Last Modified: Thu, 24 Oct 2024 02:00:25 GMT  
		Size: 144.5 MB (144534810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da134c56aa810755455a97c4cea7e4a5ccb0b07a885e4de1a8ddca03dcde6db`  
		Last Modified: Thu, 24 Oct 2024 02:00:23 GMT  
		Size: 61.2 MB (61212282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851775e1e319503f78968066a39fe865b8c6822a25b4f03be05bc14d24d84fb`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3337fb166f26558dab6047bcf9ca9922f95d8f4b94f259f9e8b9a3cf1c168df8`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cbeb5a7b057da80fe2d46b35b9e6195afdc92be855a27f3f91f04ac7b629e4ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5141035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2accb171eab041c59f4428b11e5ed7a4c1eb94f13e3d0bdb03e6f3d533915bd8`

```dockerfile
```

-	Layers:
	-	`sha256:397640157825e650737aa999b6abaaa326fe079a4c541b1cd096f782549c1b49`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 5.1 MB (5125316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3d402957d3a6bce960cd44c0fb51e9bd911749a1b976b1924361dcc8dddef93`  
		Last Modified: Thu, 24 Oct 2024 02:00:22 GMT  
		Size: 15.7 KB (15719 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3057bf59ad841303e095a7cea9a1b37f295e15d704c4c5322d5773a8ab42586f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.1 MB (233109096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678d6a75582775df45caca752ca9587cf4d6fb16935af070c055e7797eb0a1a3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60746b2d48dfb19e043609b9b09417ae53dbcb13af929a26fa77a66ad395af56`  
		Last Modified: Sat, 19 Oct 2024 08:48:40 GMT  
		Size: 144.0 MB (143959478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6b3707f40fa3f13507c9fcf22dbc220a05a4b9ba0c11a7d3890db897f233f9`  
		Last Modified: Sat, 19 Oct 2024 12:08:57 GMT  
		Size: 59.1 MB (59072819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eac767e0b14747926380cd33b795b2bbe5d074d5da95a8fcfe6ce83e8b7358`  
		Last Modified: Sat, 19 Oct 2024 12:08:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c89a593d2586a9cbe578476aa584a54e6d14228b61cbaa340e5efc299d09ae`  
		Last Modified: Sat, 19 Oct 2024 12:08:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:eed7ed0cfa86703ffa786b3c44f65b0f91b085b785940a91f7e9e950f4518a95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b09b321b4c52bb765294dc39c291af31c6b2f4241a73c79c8de1e554b97ea89`

```dockerfile
```

-	Layers:
	-	`sha256:5b91a37a6a14357e3f45f4b107851c18f53dfb09db862a1fa68ed355ccd53a2c`  
		Last Modified: Sat, 19 Oct 2024 12:08:56 GMT  
		Size: 5.1 MB (5130417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b5241fae364faea996811832af07be5daa68adf71f7b7e2873f801928cc6eec`  
		Last Modified: Sat, 19 Oct 2024 12:08:55 GMT  
		Size: 15.8 KB (15831 bytes)  
		MIME: application/vnd.in-toto+json
