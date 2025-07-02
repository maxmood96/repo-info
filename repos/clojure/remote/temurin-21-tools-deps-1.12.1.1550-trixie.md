## `clojure:temurin-21-tools-deps-1.12.1.1550-trixie`

```console
$ docker pull clojure@sha256:9717e4b949869a300ff0f5a78d0424a3c2407867fc46d84267f43edaf546e1fa
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

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1616ed7e9e82854346917ed3de67ac1bad17275cebda3fee346dbe075bbef7ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.3 MB (292254194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91884fadc6df27a66cd6331604c36ba3f14ab9c80cafccab77d5be4f5d80a6bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1751241600'
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
	-	`sha256:b72fed6e2775feec9291a4bd4b416f996dfc503eda11eaa00def55711302b4ce`  
		Last Modified: Tue, 01 Jul 2025 01:15:00 GMT  
		Size: 49.3 MB (49263877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bca81dcca9ef0c568b34450164c1191ee77c1488205ba6e445c97e61dcd3a6c`  
		Last Modified: Wed, 02 Jul 2025 07:12:37 GMT  
		Size: 157.6 MB (157634482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f187e4a4b1b37352de6d7225dc8faf80d203f99a461595b8f80ee1a1054b45`  
		Last Modified: Wed, 02 Jul 2025 04:49:49 GMT  
		Size: 85.4 MB (85354795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff029ae22ce67e932569c15f0ef3d8dc9d852d3c26bd96f9d1d65057b85b935`  
		Last Modified: Wed, 02 Jul 2025 04:49:43 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0575a8164dfe6b1b65eaaf13f403a8c9c07830f646114994c30e7245fa0e0609`  
		Last Modified: Wed, 02 Jul 2025 04:49:43 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:024a9a303a5ddbcd8f6546b45ed7ff682fe4226d316f696fac33240b7544b47a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7479388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db83ea08241131aecf491c89d6a5480dd8b3af7a4e3199d4bd6a5ef642b6a7ef`

```dockerfile
```

-	Layers:
	-	`sha256:000e4f2bdd969edba3d63c002046cc729594e567ad2ae2ff8b41f11bef38b561`  
		Last Modified: Wed, 02 Jul 2025 06:40:32 GMT  
		Size: 7.5 MB (7462923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f962cd50a047639f1f351e683f36b6e9342a8f643086f5c84e9c8c26b58e065e`  
		Last Modified: Wed, 02 Jul 2025 06:40:33 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:79735747cb1e29543c36a89f9c35445e06b8bf6682cf506e7dc783a57961ed9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290732047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f593686f34e693f219f7d18e8d569708b644439e4f508f40ab733184dd279c27`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1751241600'
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
	-	`sha256:2581a046e315a4b3013d50a17da46bcffbba144014a55d733fa55c3bafc6b7ab`  
		Last Modified: Tue, 01 Jul 2025 01:18:05 GMT  
		Size: 49.6 MB (49630154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b9e80def4c9a1d31012db33fa85b62b5dd56fca51ed6af66eefb9d462a783e`  
		Last Modified: Tue, 01 Jul 2025 12:30:48 GMT  
		Size: 155.9 MB (155928808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a407312041e31fd652507bbb24e29b479d7c76f6410700bb6e9d099b114c1c19`  
		Last Modified: Tue, 01 Jul 2025 12:34:55 GMT  
		Size: 85.2 MB (85172047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8219b9d7cc748b24795949967eb00111ca1fc2f672c239507d15b3550877431`  
		Last Modified: Tue, 01 Jul 2025 12:35:24 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4227667ba3b8ed9e2d104735edb64863808cf97e816cbf0c003acf396957d0e9`  
		Last Modified: Tue, 01 Jul 2025 12:35:25 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:71ba27732306a613175ca488b69294a808fe19a593a4a81d2e8af27c2eaf27f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7486584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd55b803549ca23aba03563ac9b600453a170b13178867bf454f5f88ff43e59d`

```dockerfile
```

-	Layers:
	-	`sha256:afb38562d57d1fdc0093588452e17519d6611307502be247d5d1c6222090007e`  
		Last Modified: Tue, 01 Jul 2025 15:39:21 GMT  
		Size: 7.5 MB (7469977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:402b3714fcef5cc62d648749703f4880c730adbb21928357bb6a0b9a0704af90`  
		Last Modified: Tue, 01 Jul 2025 15:39:22 GMT  
		Size: 16.6 KB (16607 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:a2a73c7f7dd255ce3be312e56d515367b89b433b16ec9886781ec35fde2d2f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.7 MB (301672850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70c3acd59663cc0c10b668a311a944ae2b5513faf56c8fa73fc0a96aeddb66e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1751241600'
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
	-	`sha256:5c6a246a80c20351fe842a314b6b3f8561a5ceaea736decf36fe380b29e53224`  
		Last Modified: Tue, 01 Jul 2025 01:18:57 GMT  
		Size: 53.1 MB (53097236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc7c6d506806bd280e9e75eeb1542eb6e3a8fda98921026f2d537f223a0edc2`  
		Last Modified: Tue, 01 Jul 2025 13:32:25 GMT  
		Size: 157.8 MB (157804905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4390532b3d9f3bc96819007ad3745d4065a78300330804ca7b70e72f917ffa86`  
		Last Modified: Tue, 01 Jul 2025 09:06:05 GMT  
		Size: 90.8 MB (90769667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2045fc3fa20e99f4277b33e6b0207a8894648aac1c0eda97310982379eb9573`  
		Last Modified: Tue, 01 Jul 2025 09:05:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ed406f0756a9147c3ebb875a4365e918ed440eeb11429df92ce3c008bbe0eb`  
		Last Modified: Tue, 01 Jul 2025 09:05:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:6310b795ed82954d8501157084a229589551c94ccccda9a9c2bb65521bf8d6ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7483877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d61ec7b97b0edb49c8cba405eae8734c10a6d68baeb9ec183a3d6369f21e6a46`

```dockerfile
```

-	Layers:
	-	`sha256:040d6fe88f2965aa4e7373b4522aacd158837937ea32526d39b1cfee8c725c04`  
		Last Modified: Tue, 01 Jul 2025 09:40:05 GMT  
		Size: 7.5 MB (7467352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b62da221bef854b2e17dc50df19d27e1987d583ea421e8c75f9de8edeb83c0a8`  
		Last Modified: Tue, 01 Jul 2025 09:40:05 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:e4bfee5602cf185661b87dac0e388b4e0dac75abd0636925cc05d2e30ab648ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285438588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0c7cbd0d12aa7d103ca4801a3f635dc52128fd89c50f50622e37c34d96fe65`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1751241600'
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
	-	`sha256:a19cda6d0aca0ae93b23898ddaa4518ab5077c7011f945c7a7e4a2cacb08ca5f`  
		Last Modified: Tue, 01 Jul 2025 01:23:18 GMT  
		Size: 47.8 MB (47750158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e076e085e4924513404df674a4b5cdd11b691d0a99549b6d4e3c46e86877f1`  
		Last Modified: Tue, 01 Jul 2025 03:02:40 GMT  
		Size: 153.4 MB (153449649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e031c8c36ce5ae72ae17b82b20d3b8c893dc9818b08e07cb8c2e96db91429a25`  
		Last Modified: Tue, 01 Jul 2025 03:17:44 GMT  
		Size: 84.2 MB (84237742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf65a88e6e3882ea20858b7f9d17cad52ba6c9f3bd3503b4bf5b856d18461a6`  
		Last Modified: Tue, 01 Jul 2025 03:17:38 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d45837c9073667b247badd62c98343241d142c3f8e9bd897a5d8fe9ae1a3f2`  
		Last Modified: Wed, 02 Jul 2025 09:17:09 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e73b3f94f5053bc35a083d624e2a5dc82b0b1937a04f366e99b07c77dd041ccf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7467371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15f7cea1999f56445d6bdc088674f1f6c927988f1292c25713cad0c3c05037dd`

```dockerfile
```

-	Layers:
	-	`sha256:36a920ed863e5a8bed10792b229161324cd795b5e958e4f10d3f1d54ac63eacc`  
		Last Modified: Wed, 02 Jul 2025 12:39:56 GMT  
		Size: 7.5 MB (7450846 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de70761faef6b194e4afdf1b2ae288f9c63bfb5d712b2b3db5c59512c9cb8efa`  
		Last Modified: Wed, 02 Jul 2025 12:39:56 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:09306bbbeabbaeb9b1041231e4d55634908fb1952c0bd37b8155c3a22504c55c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.6 MB (282590427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1227b7245beb5e4cceb39fa849c96837a73723ad11d658e89cb9fc2c9d4fbc2e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1751241600'
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
	-	`sha256:48de1d8f52c0a2a00375babc11bf69628b8225862d3b6ebbb2205e4ae2f3e96a`  
		Last Modified: Tue, 01 Jul 2025 01:19:00 GMT  
		Size: 49.3 MB (49343660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bc60726a2f3745d54c0dd09294d4451be8392d24b90a4488a0071b6ed0b78a`  
		Last Modified: Wed, 02 Jul 2025 06:48:19 GMT  
		Size: 146.9 MB (146910935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7bffe859bd89a61a9c2516b34aaf56b53d4a16877f8d27a33f2953516f9ed5`  
		Last Modified: Wed, 02 Jul 2025 06:54:04 GMT  
		Size: 86.3 MB (86334792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21867e9837efd16da219eb60a700722b7d20c7b0a6e64acfbbace178168f6bad`  
		Last Modified: Wed, 02 Jul 2025 06:53:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9d7fac79b09becea393d3fc379946f08297e1a0654036d20adcb64cc60dab5`  
		Last Modified: Wed, 02 Jul 2025 06:53:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.1.1550-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:f2e7ef8fc102fd2b337bfbcfc42c320e9a294834d1bc45141114ad3449469b8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7475310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a1d3f62183359626c5bc3516798d78dd23a429a91004457d6021b03f590469`

```dockerfile
```

-	Layers:
	-	`sha256:1f0ce95a478af19b5bbf2eb0a237c3ec06062d384bfde9e45bfdd854ebb74fa3`  
		Last Modified: Wed, 02 Jul 2025 09:40:11 GMT  
		Size: 7.5 MB (7458845 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cf6fe8c8d745c07205e2b0738406bdb3aabc5d999f7a66843a54fefb14ca70a`  
		Last Modified: Wed, 02 Jul 2025 09:40:12 GMT  
		Size: 16.5 KB (16465 bytes)  
		MIME: application/vnd.in-toto+json
