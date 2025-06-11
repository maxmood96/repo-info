## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:3b96fbf2cfdd2a83ec73c29adf6dbae30d06c00b687ab801204ca150ce22fb75
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

### `clojure:temurin-17-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:8d92c8e2a57090ca2335c572665f0b575690eacd08dab7d37e4109ba9941c920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.2 MB (279155091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1063aaad86ccee8a6b9df72729ae85886ea4009fb918c18995cc07b7529309bf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1749513600'
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
	-	`sha256:d8e51f6b7dcdaee60f07f9a13a971abe1be9dc977d52d0849087118f80a1c7d6`  
		Last Modified: Tue, 10 Jun 2025 23:25:45 GMT  
		Size: 49.3 MB (49253859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce605f18377f46b0245e41f6b9ec33b782e68637472728aae3a772ea426f082`  
		Last Modified: Wed, 11 Jun 2025 03:56:32 GMT  
		Size: 144.6 MB (144634963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf81afd90ef3356d75ea3ac89974b84efc469c70e20c29424684cd7c582316b`  
		Last Modified: Tue, 10 Jun 2025 23:52:27 GMT  
		Size: 85.3 MB (85265225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b945d38a6dba23d853eaa17e6e7b234e938d11ca3dbc48e2682cfb41f1bdd8ef`  
		Last Modified: Tue, 10 Jun 2025 23:52:22 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe14f91402c289a230f998c38fa897d9cd60fd2cded2e9e0eebec19693e243e9`  
		Last Modified: Tue, 10 Jun 2025 23:52:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:816133fea3e08935fd8c2ba1f51c400a64fad1397c07e56d78a2839ac78168fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7474945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e876cd36628fd5029e338bb77595fd135e8115971a4edacb8c1cd3f2860bed`

```dockerfile
```

-	Layers:
	-	`sha256:fba72af9faf2f946ed6cfceef8f45fd91414be17a1485fc6ca14f2cafb8b8d7d`  
		Last Modified: Wed, 11 Jun 2025 03:37:47 GMT  
		Size: 7.5 MB (7459149 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ddf12509772351890be6834a68efb0a8171034e73f5c72548ce9f8e9a3b34dd`  
		Last Modified: Wed, 11 Jun 2025 03:37:47 GMT  
		Size: 15.8 KB (15796 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04bb6716f76b16bf6841bc9f18efcd9242a45c4342b8f69e04f6809304e3fab9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.6 MB (281643151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78e71c64fd94b15a30ec1563d767712e1d8ea558be3713c879d4d7abd9bd611c`
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
	-	`sha256:0716c0c482281cd83847775856a8d2b5dd899b670a27f613e6c9f63273d5d058`  
		Last Modified: Fri, 06 Jun 2025 12:50:12 GMT  
		Size: 143.5 MB (143512625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b20f106202c77c1226f8e33ccae56ec009989ab360ad9e78cc99a5d4b2a32ee`  
		Last Modified: Mon, 09 Jun 2025 17:50:21 GMT  
		Size: 88.5 MB (88511193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca90f199128bc83ec050fbc662c91877c7af5995082fff9033bb3d02413e7e5a`  
		Last Modified: Mon, 09 Jun 2025 17:50:11 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07d627a61b498b34c942e540c7ab53ec7da5945558446168fa8eb0ef7948db`  
		Last Modified: Mon, 09 Jun 2025 17:50:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:fbe14280fc10e3d7659cb15c758eb8e6f74b8519e0976f39e32787fb5acda473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd0772b79940a12e59532346638d31b3f42236ae2e98147997bf51f5ebe2a601`

```dockerfile
```

-	Layers:
	-	`sha256:1c4c08c8bede2f4275a8b7478dcd3745eca9d8438e92a90debb20c3e3c4ad55c`  
		Last Modified: Mon, 09 Jun 2025 18:38:29 GMT  
		Size: 7.5 MB (7465665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f684e5a16efac745911be855112a1fc964ea04503a863b79b280fd33cad677c9`  
		Last Modified: Mon, 09 Jun 2025 18:38:30 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:7d7abb0ab69b5bd1cdad10fb99128a3fd4bcf550168b1125ec0bc7dfdc77accd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.3 MB (291312527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a039f60cd2e78095c23638642ecb0c762d057de32e88a17d6268adf36e630379`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 20 May 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1747699200'
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
	-	`sha256:25dfffa4126a91eb76c700c90bfdc9a9e15f34c7438a81f16c8a6999bbde6e45`  
		Last Modified: Tue, 03 Jun 2025 15:03:14 GMT  
		Size: 53.1 MB (53080544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002fd7f4fc1007a30b1949050f0ba69932c1032b69ee73e8eb4d85a1f11db273`  
		Last Modified: Tue, 10 Jun 2025 11:53:57 GMT  
		Size: 144.3 MB (144280585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ab73ab8b7bbe5fbff7bca9e0b133e1cecf5700bbb054c0354eff7182b6dd9e`  
		Last Modified: Mon, 09 Jun 2025 18:08:14 GMT  
		Size: 94.0 MB (93950359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2635915ddfeacab2aa4e90fbc53c31fc0912d6160c5b3c1aff1221c16af2ee`  
		Last Modified: Mon, 09 Jun 2025 18:08:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f4ed29a6c6e344d1394ad9638b333645869bac8a92a17c058261abf57be916`  
		Last Modified: Mon, 09 Jun 2025 18:08:05 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:2ad98ea53e53062e61ed208f13734a1564c85a5de41659c90f40e6a6bfd013ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7478897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2645e9392c91acb13509a3f2de91c074a894985c9daecacfffb2656495a0d9f3`

```dockerfile
```

-	Layers:
	-	`sha256:81a3ba817b2dd2b48405fc8dc04b1a8864c17e46b172e3625c58847d55bf6619`  
		Last Modified: Mon, 09 Jun 2025 21:36:53 GMT  
		Size: 7.5 MB (7463052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:588f54bf5a47145ad368cd81e568311c4462277ef4eaa463e21d6911752900ae`  
		Last Modified: Mon, 09 Jun 2025 21:36:54 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:4b6dc54b57fdf324a6a6c27580e07a87baca9d9c5fc5c8912f1758e758dedffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.5 MB (270479943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d159ecddcba7b88d0c2406c6d31a8b36e4af294b15380b31b4a99f1d401e2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1749513600'
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
	-	`sha256:183a50217c4846c3775204631f79c9cba563face97fcc3de4421f000af401588`  
		Last Modified: Tue, 10 Jun 2025 22:56:31 GMT  
		Size: 47.7 MB (47743345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c89fe622e05a06e5e344a821207a367d735cc855c9a7e163512c86f860d1ae6e`  
		Last Modified: Tue, 10 Jun 2025 23:45:26 GMT  
		Size: 138.5 MB (138492480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae10d02f66290e254fae48da0c939587567b0fa12f2d34a4a3fa7e5fa45394c6`  
		Last Modified: Wed, 11 Jun 2025 00:00:21 GMT  
		Size: 84.2 MB (84243072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:516110733157099fc4e03693f35ff995206816dd8eb84b581df2ca8fc10814ec`  
		Last Modified: Wed, 11 Jun 2025 00:00:17 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ade417cad2ddd41c17438579f1168a6468e5d189757be260290babc47f013e3`  
		Last Modified: Wed, 11 Jun 2025 00:00:18 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b49bbcc62d59b1ff54469e1e53ce1f636b3065d9748e84ff8451c8976674d6c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7460986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7001fe04866fb3894dd4f04330856f4a12a65f6365766e040428ab82a4651986`

```dockerfile
```

-	Layers:
	-	`sha256:47a5eb89cc44e9733ea02e57823acd5afc37fce8993b044b8a2e88f9ab0ccfee`  
		Last Modified: Wed, 11 Jun 2025 03:38:00 GMT  
		Size: 7.4 MB (7445141 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e38fd2a83dec07c0d7f6005e680644c5a97a39af553d5ab363551cb4e7b357d`  
		Last Modified: Wed, 11 Jun 2025 03:38:01 GMT  
		Size: 15.8 KB (15845 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:4525af4797918a9131702e40dfe46b879a2e617578ada953fce15a69bf426611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270352290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad7f48b9f878d1cdbeb942a722dc8117dd1992baee628ebb1fe3f912e9762e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1749513600'
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
	-	`sha256:1ffa7429d410cb8e2162450d6c2fc3a21121304db16d73a6b9feaa05000dde5c`  
		Last Modified: Tue, 10 Jun 2025 22:53:14 GMT  
		Size: 49.3 MB (49329768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a0b89db4a0f7f074370d21eef52d31146cae503a0f648834e534c675e558a1`  
		Last Modified: Wed, 11 Jun 2025 05:43:50 GMT  
		Size: 134.7 MB (134673543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bf095dc89270c1baa2b0a0f06ee2035bfd88f8bbeb56a8eb4645a661835495`  
		Last Modified: Wed, 11 Jun 2025 05:47:52 GMT  
		Size: 86.3 MB (86347938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc6838e3a1b42ed0653b8e32e8120d16e4fa4ee096b7786d67a96c5065754f3`  
		Last Modified: Wed, 11 Jun 2025 05:48:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7153130c6c017735ed8fb2d5b8c218d9966b187fcc19d4a2a309a25414deabf8`  
		Last Modified: Wed, 11 Jun 2025 05:48:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:4bef2439676087e0132e11becc404c6900e6ad7600d9b3ce2d536d43f7b07b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7470868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:968d7d5b1d03a42a5050ca7aa9ba402b3357bf9f77fe9250a56bc92e44eccd36`

```dockerfile
```

-	Layers:
	-	`sha256:ffaa8db1b4776edff676660654e57921cecd82f6dc4125eed5b981fd9caf9863`  
		Last Modified: Wed, 11 Jun 2025 06:37:21 GMT  
		Size: 7.5 MB (7455071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b82d523b44fb9cabfa660ba630f0785f0f92588bafed2012e411159f9d0d2ab1`  
		Last Modified: Wed, 11 Jun 2025 06:37:21 GMT  
		Size: 15.8 KB (15797 bytes)  
		MIME: application/vnd.in-toto+json
