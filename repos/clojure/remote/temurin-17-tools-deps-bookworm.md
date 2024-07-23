## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:4ac37bbda07251d90115ce4b611942faa11d04d096af5db7396ad5c021847f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:3f7c8369539d8830d107a1ce27e59f802437e28f0e5094619ad62343e8db2d89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.2 MB (275235619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2eecef98fcd998c6962a80a21a6e627170894b8aee7b2f16bce9c7107d64af4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Sat, 20 Jul 2024 21:06:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 20 Jul 2024 21:06:39 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 21:06:39 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Sat, 20 Jul 2024 21:06:39 GMT
WORKDIR /tmp
# Sat, 20 Jul 2024 21:06:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 20 Jul 2024 21:06:39 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 20 Jul 2024 21:06:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00de51947ceb8acb2cda9bf7438f9589ebb2803034aae7afffe6d49b1dbd53a9`  
		Last Modified: Tue, 23 Jul 2024 02:01:11 GMT  
		Size: 145.2 MB (145166518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9645546a2ce8faab866a742a23e3264b9e38b06c7f37e85d83386bacf51a8d82`  
		Last Modified: Tue, 23 Jul 2024 02:01:10 GMT  
		Size: 80.5 MB (80513992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74935e3395f7b0ecab7aa634b171c9e0339eeb4cbd6c25bef1b22a7162ac2b08`  
		Last Modified: Tue, 23 Jul 2024 02:01:09 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5de92dcf70038002e8cb5a7c329e87152b8e61f793fa911281d3041fb5466565`  
		Last Modified: Tue, 23 Jul 2024 02:01:09 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:953f60e2d111fb674f445a136b23f59291f2ff2a6b4ad02e5e4fd8f9c19769a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92faf22ca074264d34d8ea35faf106bbb55825d7df6cdea733f4bb0e3e4e6699`

```dockerfile
```

-	Layers:
	-	`sha256:98118580e7ce089667ed1638dcd1833cd4025fe7e71672d9bf88830b2011a56b`  
		Last Modified: Tue, 23 Jul 2024 02:01:09 GMT  
		Size: 7.0 MB (7000086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cd96d56a0396b6c3ea6ded754ca7e908e9c39d6df1604a7e1c5c852000795701`  
		Last Modified: Tue, 23 Jul 2024 02:01:08 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04b81fbd5117fb01ade3a610d89c2823ef30b32c4480c2a84238a62e439aaec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.7 MB (273744157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9805e51330b390fc93711d6daf6c0231f2a790ed90c2d2402e3f7f005de2ae00`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 28 May 2024 15:17:11 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26cfc19979ca9a99689067141093bfee8fd423e8603d7eba0c5b5e61aec04d29`  
		Last Modified: Tue, 02 Jul 2024 09:27:57 GMT  
		Size: 143.9 MB (143892731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cecf732f8b012a3cf0b695cecf5e178f4966966d687c8a34d4e64dfdefccf66`  
		Last Modified: Tue, 02 Jul 2024 09:32:26 GMT  
		Size: 80.3 MB (80261939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:238efeb339cf8ecf757e66c60dba9c4d71f13ace7b63e11cd76929973be1fd89`  
		Last Modified: Tue, 02 Jul 2024 09:32:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f587bea90699c8a197e9d8844accd6dfb4badba325aedf319ee185934f2370b0`  
		Last Modified: Tue, 02 Jul 2024 09:32:24 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:be0845b0d6a32de667916cb435df6f3c0a9213697c1cf74dd49d9568d8d136da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6982323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5010f860b51c534ee1f6b4ab8ae4c226b3c137595a2251d14c636135094c320d`

```dockerfile
```

-	Layers:
	-	`sha256:7444b966a50bbe47db6359d6b86098eccd6aac238e07a1b7f902f1aaf8716d2d`  
		Last Modified: Tue, 02 Jul 2024 09:32:24 GMT  
		Size: 7.0 MB (6966348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a498c8efcb461c9acd6c2ab0b9dbf67fd55d7d047445a03d4f8b750a9f767e35`  
		Last Modified: Tue, 02 Jul 2024 09:32:23 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
