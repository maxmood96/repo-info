## `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye`

```console
$ docker pull clojure@sha256:480309ecb23c7fe879476f46f4911c1ef096c6a5ed3420a35130d3fecf62d773
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:781563b24391d3ab92f1457ce6a3f0d432593a2d7d853dadfe51b23989c01f63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268011138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1158af26418f085ae2000f47574824ea815bb8443993c511e2faf027f776c3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:10ffc47270cd106d2d04bc7ef4749d579620e45a84804ba3b18f0898fe5ecc64`  
		Last Modified: Mon, 29 Sep 2025 23:35:07 GMT  
		Size: 53.8 MB (53756064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a0500948353142594fef1ce3d42b55822964cbb060c9c3f32c2abf383a5d85`  
		Last Modified: Sat, 11 Oct 2025 03:34:46 GMT  
		Size: 144.7 MB (144693335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d545b80f56e41684651e7cd56f54a93254e26edece9c7e71454282b5875b9bc`  
		Last Modified: Thu, 09 Oct 2025 22:28:47 GMT  
		Size: 69.6 MB (69560697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38e766b2215ec64a15783d6fdcffdf7f5653f2e26fc64571a236e71d40fc84b4`  
		Last Modified: Thu, 09 Oct 2025 22:28:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a9840cac5d0014ee65d8e0f5bbecf8c85dfb568d7daa149d0e6d1236276e8`  
		Last Modified: Thu, 09 Oct 2025 22:28:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e4f38f8b70226d5c7d8753cc64aef71924d7718c53a35169d10e63f1a6eeaffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7413112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070c13f757d8f7d183247bf8e8b0e7a3c8efc87a2286897c9b7dc54b283ef2af`

```dockerfile
```

-	Layers:
	-	`sha256:a3af64e9eea7a611ea9b9c471026a865e7e206e1075335c2deb1e47872acf662`  
		Last Modified: Fri, 10 Oct 2025 06:39:58 GMT  
		Size: 7.4 MB (7397291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33dd25dabf1e41895420c501dac604240700c9f732956b1e790cd84fbaef1993`  
		Last Modified: Fri, 10 Oct 2025 06:39:59 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fee0e3e609a420975698f3152183fb9b6481900e97cbb604e5213c25595cd666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265488770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6abcd4355b53fe7a4d88854a6005c92bc6f9e9ace1fa6fb38d2deec7a5ca329f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9b16ae1bbd1ada84c12528379a10e280bd89e0d0332670c8487145eb77fe2fe1`  
		Last Modified: Mon, 29 Sep 2025 23:34:42 GMT  
		Size: 52.3 MB (52257414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613bdaae7b8005bf7060280a91945faecfcedc13e625a6f40685665252f6c708`  
		Last Modified: Sat, 11 Oct 2025 03:35:38 GMT  
		Size: 143.5 MB (143542147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3029ef7740ab7e0b26fb2f527c36cb18b53b7198220c065c07c62abd284451e8`  
		Last Modified: Fri, 10 Oct 2025 03:51:05 GMT  
		Size: 69.7 MB (69688170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7fc556cd45784c247f58b5a4c4d9f61b65a35d79c9e3625a0ed0d193cc808f`  
		Last Modified: Thu, 09 Oct 2025 23:11:50 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a828a3188cdeb19dae91397cab8db11228ade7b1b94c8eb6e153612429d68f70`  
		Last Modified: Thu, 09 Oct 2025 23:11:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.3.1577-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8b28d9267dd76f1a315301daaba7d230315829a196fc0d37d9b9449ef7eccc0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7418329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a06682a895724dbc824d14d60218c9a07938afd02ca64dd4f5ea716b5cb293f7`

```dockerfile
```

-	Layers:
	-	`sha256:af00c52739d6bcfe5e949f43986d479709aa11e3112255eafd366abbd0c2f6bd`  
		Last Modified: Fri, 10 Oct 2025 06:40:06 GMT  
		Size: 7.4 MB (7402390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38f01db917954abfdf645edb7dfda9d65e265dd3ef5dda77ce87a14d8b045ef7`  
		Last Modified: Fri, 10 Oct 2025 06:40:06 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
