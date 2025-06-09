## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:4d6797c8d53d1556618ef9a953699378293231c2122d69bf023768fd4bf50b13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:70149514587147f41256513d723cf60c5a48af683751d73782c9deb2762dd582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295089148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f5e8b59904221f4284ead255714a818403a722373abeafd3060d8db9851214`
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
	-	`sha256:8f74611b5dba7cbc5f019083facce00ab400dbe2b351065920462c7d8e1bec20`  
		Last Modified: Mon, 09 Jun 2025 18:56:53 GMT  
		Size: 157.6 MB (157634484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5aa75b07029e7a3bcf721619b7afb3ce852f7a856538a633b4e4a0f641c5cc`  
		Last Modified: Mon, 09 Jun 2025 17:19:19 GMT  
		Size: 88.2 MB (88206713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a512d823b7578b45e28b87a33b6c7514b295ade986e692988e80ab018409f53`  
		Last Modified: Mon, 09 Jun 2025 17:19:02 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b433ebbd7db913bb58e795f9e49d4e1d1d5102ba586e62d387ab92955e22d343`  
		Last Modified: Mon, 09 Jun 2025 17:19:03 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:0164f9a18cd8f2a380e659dd128d9d21a74a0e111b132a980044cfc04e432d43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f48b520aa9bb904b5824befa15286bea172fefcb33ecf5144948c562ae9e27f8`

```dockerfile
```

-	Layers:
	-	`sha256:0d2d1f28075e902a895cc4d9434c0a89d70d8e278013ec9126f6279983dce1ef`  
		Last Modified: Mon, 09 Jun 2025 18:40:10 GMT  
		Size: 7.5 MB (7462405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36d15b031ac0b52c1bc69df803b35b8ddbbdbd144a52493a7415284a049fe38`  
		Last Modified: Mon, 09 Jun 2025 18:40:11 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2bcc3bca708f6a45d319d0736dc9d1102d888a9d540a21a263b78249d6b7249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.1 MB (294058913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1567c4c5390636218ab5d10c23e05301c884a1c5d6bc97b7e1b2ea9e089a92`
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
	-	`sha256:669209475ccf588005064aec8b03f795116e849de02f62977a14a87f1ef3e90e`  
		Last Modified: Wed, 04 Jun 2025 11:30:41 GMT  
		Size: 155.9 MB (155928831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874a8cbbc40e5a14834f27ff81176f9ac59f0a77cc90a8d86bfb898c8951daa8`  
		Last Modified: Mon, 09 Jun 2025 17:56:32 GMT  
		Size: 88.5 MB (88510747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8859b47abe90da8b5343cbed330755c3c8b247226f670b902299a33a631fee13`  
		Last Modified: Mon, 09 Jun 2025 17:56:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3a597e9808f5cac0cd0b776fb75c88ae77c7f242334092cafcd08436776fe`  
		Last Modified: Mon, 09 Jun 2025 17:56:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b5d2d5a3b6af6fee9a32de57a4f215d74e19ab9c4ce6c6797b7727c9101dc01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6ef5a6c0a820252f1007281fde96249689e9d3314e70615367bd0a940b0b785`

```dockerfile
```

-	Layers:
	-	`sha256:43bc8aec5b2c489dbac7bb21bc4764ea920274a52028b5deaa461bf9be86353f`  
		Last Modified: Mon, 09 Jun 2025 18:40:17 GMT  
		Size: 7.5 MB (7469459 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb30620d89090349e8195ad99557bfd8e7e1c946df92f65d9df2d78e70ab91a`  
		Last Modified: Mon, 09 Jun 2025 18:40:18 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json
