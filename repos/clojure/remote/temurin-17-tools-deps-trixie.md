## `clojure:temurin-17-tools-deps-trixie`

```console
$ docker pull clojure@sha256:68d603a8088d1eb8015a2f1f4a5e49e8383e115e759a04b7b9c2246033406ed2
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
$ docker pull clojure@sha256:6f6c098079693474a0c8f1ca3f1344afca06cddafa5134e74ab690d9993d6997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.3 MB (278331739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa5db5e644c6eadc86abe70315820f2b22203bf6e0f26a4846ad41e03e5c7720`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1749513600'
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
	-	`sha256:546a427a0109bbde3a869c6a4ff1ed90ec74768e7fd82dd00441608d83416632`  
		Last Modified: Tue, 10 Jun 2025 22:52:49 GMT  
		Size: 49.6 MB (49621528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a6a72e475a5b55de2eb90497671caedc20f1da6c7e5ca00aab0d3c77b204c6b`  
		Last Modified: Wed, 11 Jun 2025 08:27:24 GMT  
		Size: 143.5 MB (143512615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10a429b9ffd932e4ee40499cd0468f6cf59e332542cb5043cda50e18a1e90a4`  
		Last Modified: Wed, 11 Jun 2025 08:32:50 GMT  
		Size: 85.2 MB (85196554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db7fdda14d7dca50d9da52df66b022c6fc71f04ca5589479fe099636b533462`  
		Last Modified: Wed, 11 Jun 2025 08:32:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46962a463fa93df701a440a16396cd8017302d1395350eb0413b23f622feb9a3`  
		Last Modified: Wed, 11 Jun 2025 08:32:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:ac41783164b51e6bed71eb7c736b0d518da9426ba43786f6ba29fc6f1be12aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7482093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69cd48084c66a2a0acb459127d9849080ec433b5b16b9214b1dffc72e07e1423`

```dockerfile
```

-	Layers:
	-	`sha256:622d8fb9dd698c1cbeffabdcdbe8f783740e673d2c8c0e773464752777750de6`  
		Last Modified: Wed, 11 Jun 2025 09:38:47 GMT  
		Size: 7.5 MB (7466179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f355180a8034cf738201d8c01eec7ae1ef16ca83dfc848f0ea5d76e0f9b43fe`  
		Last Modified: Wed, 11 Jun 2025 09:38:48 GMT  
		Size: 15.9 KB (15914 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:1bc52dda926a57cdf91d30d15081918eaa0e5a64ddf1be4a928ca0e7c8464de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.1 MB (288144590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2246d5f3cd21e3a6485690117e328072f7cf6eadbecb4f0e3b3265adbdf5f2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1749513600'
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
	-	`sha256:70a0e6b9f26ae2a311f0c79d7ff095922eec7e2aa39f94bd8c4e5b385cfa847d`  
		Last Modified: Tue, 10 Jun 2025 22:52:26 GMT  
		Size: 53.1 MB (53090933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44989ab7095da3e326638a4f6ed52b9cf7d2a8700a6bdb976f59aa1c7f82e5b2`  
		Last Modified: Wed, 11 Jun 2025 08:29:15 GMT  
		Size: 144.3 MB (144280553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5052098f3f5da5c0f7f3069e3744966f8611b7db79de4beb10a297e3b498ef`  
		Last Modified: Wed, 11 Jun 2025 08:35:57 GMT  
		Size: 90.8 MB (90772064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2712c7f8de149270e4d5a0a9cf216f5c3a52554ba2980666e4228987e8a66f`  
		Last Modified: Wed, 11 Jun 2025 08:35:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0624de7db485a9916561d37b33546e980dba54c989afc76c214d0cae48cb776`  
		Last Modified: Wed, 11 Jun 2025 08:35:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:b44f855b4eb9ae7db8beb214611ca21595d6f3c287e488b6374483ee998d3b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7fd36f5071e22b494e41994b5e4dcafaaa373a258473e8b321248f5b5202b1a`

```dockerfile
```

-	Layers:
	-	`sha256:4994cabb0f3d6f926341e69954334f6f8e34d72167e8fa089b43501147fc02ba`  
		Last Modified: Wed, 11 Jun 2025 09:38:54 GMT  
		Size: 7.5 MB (7463566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4b0e92949e52e6f7dd35783ee2941c07e3d3bc87a04a6aa69f521414ade067a`  
		Last Modified: Wed, 11 Jun 2025 09:38:55 GMT  
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
