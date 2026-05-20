## `clojure:temurin-26-bullseye`

```console
$ docker pull clojure@sha256:f87e9644d464c5530596a83ec2691f25c15196acb6e3e6f8fb317db2cc85cc08
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b93066c492771b5584871b524de18496efe28515db2aefbac875c7605825b5df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217896322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d389c853f6f9e9ae0471feacc1d6a587e42da8361a7f9d4afbffb66b27612aba`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:02:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:02:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:02:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:02:45 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:02:45 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:02:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:02:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:02:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:02:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:02:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11a87fe12f008a1824824308a6601af4b4179a21f3332bd52209d3b185b9942`  
		Last Modified: Wed, 20 May 2026 00:03:22 GMT  
		Size: 94.5 MB (94524386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2c6160b9485a66043f5131781797e64450e6747dffe18910eb1447a51df1db`  
		Last Modified: Wed, 20 May 2026 00:03:22 GMT  
		Size: 69.6 MB (69602043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44811d7a7e6b45f115acc6c8d9ad5be079adee85c3e1f1f141cbb87480c089d4`  
		Last Modified: Wed, 20 May 2026 00:03:19 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bffb01e324ed1500f81f37250c3787e16377670e8bee97abb5174437e208ac9`  
		Last Modified: Wed, 20 May 2026 00:03:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:86850c6bcf138e306ccdf54fcc129c9ec32720d5e3a56a2ab72853d61e9c17b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7389094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88bd662ceb2c1006a359fdc4234d5ce8c9d6bb1f948dd6cdc201890b293ce9a`

```dockerfile
```

-	Layers:
	-	`sha256:dc05a6bf9d9a728c89187e92f3d9cf86d2f322874a0d7edfa2c28776a2ebd23d`  
		Last Modified: Wed, 20 May 2026 00:03:19 GMT  
		Size: 7.4 MB (7373169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c962b56a788f4bb4d92133730e4b18c3823f84e9ecea653b1d527b9995e1156b`  
		Last Modified: Wed, 20 May 2026 00:03:18 GMT  
		Size: 15.9 KB (15925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6a2479b6673b532166421dc71f0303c5a3595d3ac87f01874a96afaa84fa23b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.5 MB (215532980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9acae9eb4ae73a958161b73fee9d0f33306f3c642a310fec8d11c6abe06a92e4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Wed, 20 May 2026 00:09:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:09:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:09:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:09:20 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:09:20 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:09:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:09:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:09:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:09:33 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:09:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d4456183e85bba58716b204dd25212b07326f45e3edf7eaf2918454231edc7`  
		Last Modified: Wed, 20 May 2026 00:09:55 GMT  
		Size: 93.5 MB (93504335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e18cf9c1dab7ee43e3772f6babdf4ad99c2f7590e8dd57aad525a558ff7ebdd`  
		Last Modified: Wed, 20 May 2026 00:09:55 GMT  
		Size: 69.8 MB (69771025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2a9ad22bf2c4daa3eb4a313f5bfe5632e3d769f08623440ae681e260e0f2af`  
		Last Modified: Wed, 20 May 2026 00:09:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f2662a7064add95dbaa08ea18e7c96304a2ff780e4fb3aaac3112978b349b6`  
		Last Modified: Wed, 20 May 2026 00:09:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c49220563ea07e1dc68a5c8c2b5a232565986bfb60ac17e695b1fcfdcd992f8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ddd7ce0015862ae29d01bc89c337cac9ecf0c82418c3968c2d6d68b5816cc2`

```dockerfile
```

-	Layers:
	-	`sha256:f32dd14e2fbc5d0203e1a0742e5bee72b179cc2ae29d3a5621042549799d84fa`  
		Last Modified: Wed, 20 May 2026 00:09:52 GMT  
		Size: 7.4 MB (7378265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02bb84ddc57dd29a6a872e25ad75bf28427166710e629842293274b2340228a9`  
		Last Modified: Wed, 20 May 2026 00:09:52 GMT  
		Size: 16.0 KB (16043 bytes)  
		MIME: application/vnd.in-toto+json
