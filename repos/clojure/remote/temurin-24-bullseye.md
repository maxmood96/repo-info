## `clojure:temurin-24-bullseye`

```console
$ docker pull clojure@sha256:0b88294fdf67def2bd9267ba345cf66b0daaddcbd104e504454b89bd73cc97e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:60d3a7a336b7099ffdb284ed63ad6d1b1d6cd60cc3d8e3cd270cdd87d090cd70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213097151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff9aae2580993bb946bf85781cbae1c9aefb66bcc5278cbaa51ba7e16dc32ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca3bb53cac4198316747ad0058ae80c4d2ce9a97414c882ae79405e9e3572ef`  
		Last Modified: Fri, 09 May 2025 13:05:21 GMT  
		Size: 90.0 MB (89952019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b5f850a0371fcf16de5a7d053421aa50b6c262949f537f5ced30900c048b245`  
		Last Modified: Fri, 09 May 2025 13:05:21 GMT  
		Size: 69.4 MB (69396352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa394332b4026e41a192eb1ade9b4d1418771f8b1305044e6d532d27bef3a65`  
		Last Modified: Fri, 09 May 2025 13:05:13 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db8959bc891635c7ba413fffaf3f0059a2f63f4bb4c41054c6631e56e58e4c70`  
		Last Modified: Fri, 09 May 2025 13:05:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3718502d1143a3d87957376fa8a23f9be9279a3ecc621d80b82a29959799e54e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7173015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46d6687e594a89bce978163c3db22b32a2e778bc87d0b9b6dec705f7f473f006`

```dockerfile
```

-	Layers:
	-	`sha256:de4c1f5ad5453ca62bac60e9f4196d025242d8e75ec64db05ed2bd0e26ebe25d`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 7.2 MB (7157201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ddbeeb659894461f0dd78b16f1d9c2b1716692b167b7280ead49d0ea3fd9e0d`  
		Last Modified: Mon, 05 May 2025 17:08:23 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6195d24e024ffbd9951a794b9307a7475b69a0c02f8a8bbd6c63c3fb0f0856a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210867847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aaf2a9a2a44c0ca81b5fff913c07d359097cb3ab61dee9b9f4a0c8da45f5b88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea499e9a6440c89518277b243ca49b2d9515371f555e0f6fb5ae8bfd73d843e6`  
		Last Modified: Wed, 30 Apr 2025 01:51:08 GMT  
		Size: 89.1 MB (89091271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d647400935d43344d8fd0006b65eedc14a5dcfdb1a2e671ba2461d208eb2f1`  
		Last Modified: Wed, 30 Apr 2025 01:51:08 GMT  
		Size: 69.5 MB (69529557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aefe9a46362a5361e8561468f5f372b043300812c3e534642560ecf59dfc2adc`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ba61a959a7027eabf5c73312b56c2171dd659a136e3d537f8ccd2541f7752`  
		Last Modified: Wed, 30 Apr 2025 01:51:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1585f09ba112fc761f7ab02159e235b114cb33bc2b726b0f8cadf52d25b59986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7178229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cedf174e47155ca9dabadbc76b6941be233d17a29d25c04420bcdea448cfcb6`

```dockerfile
```

-	Layers:
	-	`sha256:f243e2a15ef98ff6c56650efc4b6c98de1c855e57fae7e7c021b0f4a92ffd37c`  
		Last Modified: Tue, 06 May 2025 00:49:53 GMT  
		Size: 7.2 MB (7162297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ff35995bfce347a4faf86a243040da484b7569c236c71d624e26d1cb9400c17`  
		Last Modified: Tue, 06 May 2025 00:49:52 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
