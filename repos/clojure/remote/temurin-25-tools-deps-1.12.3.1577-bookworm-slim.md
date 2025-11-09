## `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim`

```console
$ docker pull clojure@sha256:b721b306cb7ce0eb7cb71d483dfc075e35431bc9805c64167ff9de8ebe3b056d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9f3be1e6a0a0d341d1dcaf9687ec57d1a1f4b0cad4e7953f6f28c87529d31751
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.0 MB (189954704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d4200431c553a5aec093e4c1834edd207e0e37d1d8d835fd0e296757cebf4f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:45:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:57 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:57 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:46:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:46:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:46:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:46:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:46:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1adabd6b0d6b8acfa4ad149a984df0977135a7babf423538c7284a02744a4ee8`  
		Last Modified: Tue, 04 Nov 2025 00:12:15 GMT  
		Size: 28.2 MB (28228567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:421582664da4740bb768fd6916c10b218d30eb1880666dae91d21c87a6e92e02`  
		Last Modified: Sat, 08 Nov 2025 18:46:56 GMT  
		Size: 92.0 MB (92045315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99559910ce925747406cacfa0648277f37e73315d840013cda8998ad00330250`  
		Last Modified: Sat, 08 Nov 2025 18:46:52 GMT  
		Size: 69.7 MB (69679779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0063dea7b91a3894ac7fd627fcc3d30afd153af485a4861b877b12646380f1`  
		Last Modified: Sat, 08 Nov 2025 18:46:47 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650357fee04a56f85d612f51d50d96452d8a542cdb893cc4735c93124a05efc5`  
		Last Modified: Sat, 08 Nov 2025 18:46:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cb6b6a2c4a8158a0e197afdc074fdd1d621d95d0c7589171611417460ac158e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5081271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae1fbcdbaa2c6aea6ee7150d672989be894dbd64e2e2bd62afd42ac90191879`

```dockerfile
```

-	Layers:
	-	`sha256:9bd231d74dcfa91c27248b243d483050e04366bee71f4197365ec866a9e90bec`  
		Last Modified: Sat, 08 Nov 2025 22:51:09 GMT  
		Size: 5.1 MB (5064748 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e37612299db36b311bb1a02d76bd8f2df555faae4d361c59810c217eec3b2889`  
		Last Modified: Sat, 08 Nov 2025 22:51:10 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f948d3a4af7f952579db21b0cb1b99862ce731e92fc349cac6607786e1aa76e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.7 MB (188716250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e32a684b43411877ae989eee4f96ab6d94f47341321974b6616d27b0d4cf66`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 18:45:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:45:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:45:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:45:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:45:34 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:49 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:49 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:162e72af9357868b8f7f48fbf3ea23ddd179a309a9f28f2802a2e785239ec09d`  
		Last Modified: Tue, 04 Nov 2025 00:13:06 GMT  
		Size: 28.1 MB (28102376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e22879c5f82cfe6b85d92ef4a468b61f6ae3e7a38d234a812e91f2da9323f1`  
		Last Modified: Sat, 08 Nov 2025 18:46:45 GMT  
		Size: 91.1 MB (91052521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a47ccdd885d8364fddbc3dbf57f913663facdbd0524e2d1582ba64604c67bc2`  
		Last Modified: Sat, 08 Nov 2025 18:46:43 GMT  
		Size: 69.6 MB (69560310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f8933bb10549d0c9860efeab6ef00058d602d891735b2473fabacf18aa7c4c`  
		Last Modified: Sat, 08 Nov 2025 18:46:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b104a6357d9752b979a3473e57c7363d97b5bb37925238157d96e102a77a0d98`  
		Last Modified: Sat, 08 Nov 2025 18:46:38 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:592baa4482bbb7545d56c243b2af0c4d7949b973d8517640c18d82c44e6e5695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:173132fd2f27ef9a4b2120eec2de0343a5ab5f180693eca6368616249058ab8c`

```dockerfile
```

-	Layers:
	-	`sha256:ff53435feed473b3733fdd6330a51cae87e60b38a34c58bb424620bedd8522f3`  
		Last Modified: Sat, 08 Nov 2025 22:51:14 GMT  
		Size: 5.1 MB (5070530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e81b07df848b42355d86310a2dd16855642975baea6ea02e60f141934a49d7ef`  
		Last Modified: Sat, 08 Nov 2025 22:51:15 GMT  
		Size: 16.7 KB (16666 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:53b11285a375cb3f009dd56f174dc9c577b161475b60521307ef6b503302b733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199194052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ebea39ae746c133b338e45e757cfa080c594317c5f61ba9ff9e546510ac779`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 21:46:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:46:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:46:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:46:54 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:46:54 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:54:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:54:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:54:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:54:44 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:54:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2442ae4ed78d32124d4f8b92ec0b1caf0e12483bafbd1803659dc391d3600616`  
		Last Modified: Tue, 04 Nov 2025 00:13:59 GMT  
		Size: 32.1 MB (32068905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1965d7bccb021209291d1051f699e8f11ed0f5b51517e9c23eee8d574faad746`  
		Last Modified: Sat, 08 Nov 2025 21:48:12 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0054dcc07af215c789b54b91a914591512e44f11fbe1fb171b22a622fbb3d3d`  
		Last Modified: Sat, 08 Nov 2025 21:55:33 GMT  
		Size: 75.5 MB (75513353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e931568892ad7177dcea52886b4258175619fa6863d0434664394cb2f9e7d8fb`  
		Last Modified: Sat, 08 Nov 2025 21:55:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:198fee14b0ba56095850b7a029e17583f64fc8cb096e3fac0c9b1fc8782be8ec`  
		Last Modified: Sat, 08 Nov 2025 21:55:26 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:9a5cb72a1a3fb1b96338c7487b92d0981c3425e8f42344d8068e5a74f0823012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5087800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d8828f38dafd927f9f2b399c9b9d56b8abf33de24c01fbf1982cc7c78f2a7d6`

```dockerfile
```

-	Layers:
	-	`sha256:b403d526d9b37b73b7fa9503a39923da3b6ec9dd6595751d1e13111363e5efb9`  
		Last Modified: Sat, 08 Nov 2025 22:51:19 GMT  
		Size: 5.1 MB (5071216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc432a3e6368455bce06a7d0c599832c0995663f2a3dc34d891679fddbe5eeda`  
		Last Modified: Sat, 08 Nov 2025 22:51:20 GMT  
		Size: 16.6 KB (16584 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:9e7e16b295a018960cd2c97286a64c8a76196754945097d5da8a628c98fa6ad7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183587211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54e690109488f358a264b382d918b5c8b0f58899048ac2815bd6dc2d31546bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1762202650'
# Sat, 08 Nov 2025 20:37:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:37:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:37:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:37:37 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:37:37 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:42:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:42:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:42:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:42:46 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:42:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4107e012a4177a1e96e325eb10e9dcf20c399a18fb04e8ea0ee134870259b436`  
		Last Modified: Tue, 04 Nov 2025 00:13:09 GMT  
		Size: 26.9 MB (26884551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15694db20fc231107b78ae3d18f60c3e913b30a3c838b3ce528e37cb812d9985`  
		Last Modified: Sat, 08 Nov 2025 20:38:23 GMT  
		Size: 88.2 MB (88210738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb227391af155fdcf8ca5be85ea9b751e792a3bb6cd3cffbe40c8b3938aca41`  
		Last Modified: Sat, 08 Nov 2025 20:43:24 GMT  
		Size: 68.5 MB (68490878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b30fcc340631beca0cf71734cce91f5d6fb7f98a8cf9348c9ae7fa108ba884`  
		Last Modified: Sat, 08 Nov 2025 20:43:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba509c1bb0320b72cd19a71dfab9055f05e372045cfce756648d8b967dab424`  
		Last Modified: Sat, 08 Nov 2025 20:43:17 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.3.1577-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:10a06f35c18df04ebbe9a3603e1bce89b9620b9dc043e6c2e12f763583ab96ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5075142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc5199b7035a7bf0e7e5d9ec96d44fabcd2ea8f878b7a805cbc21f69d9a3924`

```dockerfile
```

-	Layers:
	-	`sha256:959ab9bc516e4825f09e3a64699bacc3fdb4083c3396a49bfa9617d1db7d1a79`  
		Last Modified: Sat, 08 Nov 2025 22:51:25 GMT  
		Size: 5.1 MB (5058617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80b4408f966c5df920ec2790d435f36484f32bf1d4a8314ec674b26355a7d373`  
		Last Modified: Sat, 08 Nov 2025 22:51:25 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
