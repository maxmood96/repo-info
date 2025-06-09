## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:bde53c2d5fa735b6cdc08ff750251498afccead0817e8b18190117436c4effd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

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

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

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

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

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

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:e2149556388d4becaa1dc35657a5706321c4e8686ca1e61e15e6d7cb8755b3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.8 MB (304837179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a03f581cc035150b90200f8a88409640b4e91b2df80de33425c3e9286ff04f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f6bd552c8941351aec1fc10e7be3cba78443c32cad3ba1481c6ebefe465a52`  
		Last Modified: Tue, 03 Jun 2025 09:11:02 GMT  
		Size: 157.8 MB (157804856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b61c04060a68e4f861233e6aa44907e4c977d252ad139304736358bb36ce91f`  
		Last Modified: Tue, 03 Jun 2025 19:07:08 GMT  
		Size: 94.0 MB (93950738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db78e52de32a0b285a0ef7d1c5c69ecdc8a23db606741509f7e5dd10afe2b56c`  
		Last Modified: Tue, 03 Jun 2025 19:06:59 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064d7dfcc9aaca4d8eee07a937c89b2f2a531c7faf67a17bd404bb086d961f6`  
		Last Modified: Tue, 03 Jun 2025 19:07:01 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3047ed82b174d4cb429fb38c933280023dfd76ba28bc45cef585982d3726570d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7343140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9ce196f9a783e3a30a54865a6811de5ed693bc3805cd5b09cc729939198704e`

```dockerfile
```

-	Layers:
	-	`sha256:3eaace5a72ce7464ecdc541584c85b6c7cc9a112f51181287dfa50a18648deba`  
		Last Modified: Tue, 03 Jun 2025 21:41:39 GMT  
		Size: 7.3 MB (7326615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76b3d5dc66fa881586ba062fd0e8ecd51e9b02230f56cc7ff39d76ca468d3f1`  
		Last Modified: Tue, 03 Jun 2025 21:41:40 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:00224c6228a0779f0d43a0ed0b3ad7633fbea6877d086772d9a2a6087271958e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.0 MB (288037772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81efaeb6bb424b5c064e1a0554bda493b739251c3f18a511c95e6f8bbae90a1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c83c5fa20952cc8610d790073e97537e7832127593042fa9c620fa910fe6f6b9`  
		Last Modified: Tue, 03 Jun 2025 15:26:09 GMT  
		Size: 47.7 MB (47731411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df655a63a53f1eb7344d055b3a0a02078ae226dc1a077e6b3a1117732b72b764`  
		Last Modified: Tue, 03 Jun 2025 09:38:50 GMT  
		Size: 153.4 MB (153449622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b509a4a82e5518079103db459c9b892edfd7889378deeff2a6eb645e8d24f13a`  
		Last Modified: Tue, 03 Jun 2025 19:00:59 GMT  
		Size: 86.9 MB (86855696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d423a80a641b585765f9b56ca76b369c6568e81f77c04d4e6b0b51502dc0478`  
		Last Modified: Tue, 03 Jun 2025 19:00:51 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22d28c39f3d64ddb417af35460d807c69ee5c2bab0ca4021f7ff8fa703a00ad`  
		Last Modified: Tue, 03 Jun 2025 19:00:52 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:5da445650a64519acc6896a586ff7c9efdfc230b7eca57834da1665f3edef575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7326634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4606d50f26d500b6d4160fb04b7c0258dceec801066cd5c2c43222543126ae96`

```dockerfile
```

-	Layers:
	-	`sha256:42cd2c431fbc992118b829347b784ffea95ce7deb8a371c732d061dbc363ccc8`  
		Last Modified: Tue, 03 Jun 2025 21:41:46 GMT  
		Size: 7.3 MB (7310109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cff28c6adbe7404accb7a9a8117ecad4610c897b6e3afc9ca0860495e85a405`  
		Last Modified: Tue, 03 Jun 2025 21:41:47 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4cc8832e7326e3654b2071f71ca51b4013d5967be4a137ed417a43a62f8d674b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.2 MB (285186943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd520cf560bfe6c6b036798916a075daf711780c1e3c422d56438185ae7b2d21`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1747699200'
# Tue, 03 Jun 2025 15:45:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Jun 2025 15:45:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Jun 2025 15:45:26 GMT
ENV CLOJURE_VERSION=1.12.1.1543
# Tue, 03 Jun 2025 15:45:26 GMT
WORKDIR /tmp
# Tue, 03 Jun 2025 15:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "09b7b8185b8a35b1ddcc9c2a5155d094fe1237805c24489312f3e324a83b0d4c *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 03 Jun 2025 15:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Jun 2025 15:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71c8524b25c34592c256fbae9045d0ade48f5e9889d37c5b2190092fa9017d48`  
		Last Modified: Tue, 03 Jun 2025 15:34:07 GMT  
		Size: 49.3 MB (49322227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:861de86bc3adcdc8dc3323ae415856608e017573655a6d8e472b10aef094a90f`  
		Last Modified: Tue, 03 Jun 2025 06:28:03 GMT  
		Size: 146.9 MB (146911014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d8f26dec31d90db90070c5ba6cea64fe5dd5de50159bfacc617dc1f8d66b1a`  
		Last Modified: Tue, 03 Jun 2025 18:41:54 GMT  
		Size: 89.0 MB (88952662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42791148ff0249cb693ac3cfb7b6f057107df4d1f8767d00ffaf999e2c407bc1`  
		Last Modified: Tue, 03 Jun 2025 18:41:46 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29f1380ff7d7b33be17b9dbd80154755904c2cbc47f2682edfc8a462b0298a6`  
		Last Modified: Tue, 03 Jun 2025 18:41:46 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fa92e07ef2f286c7bcc05733cf9be5ebf4f9029b26df445c39e7c39660d7cc46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7334573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e88002c392f4f68049d360a742c56d0e4a14f0b1f12a1098251e1af226d6c04`

```dockerfile
```

-	Layers:
	-	`sha256:7ae6caf0f959612bec56919bd4954005f34a90c2137afc48bc64700dcea9673b`  
		Last Modified: Tue, 03 Jun 2025 21:41:53 GMT  
		Size: 7.3 MB (7318108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e89dd1353402b363589bf86f738bbb11246744caa8a743e68a11d5edb01dcd60`  
		Last Modified: Tue, 03 Jun 2025 21:41:54 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
