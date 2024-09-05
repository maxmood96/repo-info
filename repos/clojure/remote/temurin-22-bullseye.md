## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:eb92d11206c5c5c61bd8c0ef743bd63a049d9cba9662ccf49a6b2165d13eb712
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:864b95f37683934e359a57f0b1e6082df54ab685a8db9f1c00bb79e9da1509c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.7 MB (280660581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0f669465f812258af41c9b5b09d191e88daafbbeeb5583965e9a56d0e4933f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ac091bcd518a016679273128063f24fdbf0fbb571e9350cc89432a1e77d804`  
		Last Modified: Wed, 04 Sep 2024 23:08:14 GMT  
		Size: 156.5 MB (156481605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c997f29e5b83fba8d418af4ccab43966216c2bcb773c058797bce243a310d1`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 69.1 MB (69096608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc46d1b9dffed68c2e01d8021d38872d4e252829112c17080d4d2a707f04a8a`  
		Last Modified: Wed, 04 Sep 2024 23:08:10 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076a8a9b90b71b9fa97066ec59ad68efbd20d20f16f7939347ef90d07f105975`  
		Last Modified: Wed, 04 Sep 2024 23:08:10 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c2e7c7adeb52aad51bbd21f6546ec001456baba9e421b92e18e7603b369eb27e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50611a185b8e5ca20ff122bd1c7c25dfddfa7f17fd05bebe36a944ccbbedf625`

```dockerfile
```

-	Layers:
	-	`sha256:251f130a121bbbac0734556b15a8035d5b7fba27df1e97c3e035780e8fc0265c`  
		Last Modified: Wed, 04 Sep 2024 23:08:10 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d5334b7ec843ebf1016620f37bccf5881fd1124b6f8b4e75a6412d68467ef09`  
		Last Modified: Wed, 04 Sep 2024 23:08:10 GMT  
		Size: 15.4 KB (15439 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a6d9acf606fa09e8f82db05ac965efe1a6105ea3bc195c978bb609b928822fb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277328095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3090d40a4506497e51d5c06c520c27cb1037bdc651fda9dc539b534f822f7e7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458cd2a281eadaecc5ca931234450d99480ba147d820624e2c5f6ce0dfc7072c`  
		Last Modified: Sat, 17 Aug 2024 06:35:12 GMT  
		Size: 154.5 MB (154503707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6374be60fde5771f326f374e91c9ca919f1da972a99a668a91f36848db07fa`  
		Last Modified: Sat, 17 Aug 2024 06:40:34 GMT  
		Size: 69.1 MB (69093426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e9d78c0109b29debb2a19e234d3d15fabccca8f536d1359462506073b2596e`  
		Last Modified: Sat, 17 Aug 2024 06:40:32 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9857c8c34a5ab923c55f096f1d33c7c6f430514f7ddf9fa28c54c7822990bb72`  
		Last Modified: Sat, 17 Aug 2024 06:40:32 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:3721d67e31f364bff7c73f4d1a05bfdf19a43bf7379a15a96183c13eb812ed06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1bea3484a1b5a1302a8493446fe908ecd916383d22cdbd0c95ebbaba67c70e3`

```dockerfile
```

-	Layers:
	-	`sha256:082ccff763413b5298069287d9f55430cf4ad56b6d73cb925374eee5ebac6e7a`  
		Last Modified: Sat, 24 Aug 2024 00:11:38 GMT  
		Size: 7.0 MB (7046060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca46bc0066483e1521042f2fd31ddf8ed08e9655be3076eef7694a10248b5239`  
		Last Modified: Sat, 24 Aug 2024 00:11:37 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
