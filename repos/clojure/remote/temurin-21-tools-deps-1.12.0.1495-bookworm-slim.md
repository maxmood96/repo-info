## `clojure:temurin-21-tools-deps-1.12.0.1495-bookworm-slim`

```console
$ docker pull clojure@sha256:4329aa8b0a2b4e15ff3f029d57f9580baec7f6dfac10270541a9e83f83d0b309
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-1.12.0.1495-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c65f1f9a7c7a9fde83f8ddb49246b411abbc74d3625dcc930af2c45993865664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.1 MB (255113835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77e905f6530da5681f0d419ee8f93de9a4ae33799ff7db5aeffab4ffc085eff2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:031a76105fbddb7f7ecbab670728fccda22122d1f5dd5eb829b1fdaa60f37849`  
		Last Modified: Tue, 07 Jan 2025 02:29:40 GMT  
		Size: 157.6 MB (157568693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaea187e0e38702ddd7e1055455a799e5c9d2fb3bf26ed1620eda78e8e138002`  
		Last Modified: Tue, 07 Jan 2025 02:29:38 GMT  
		Size: 69.3 MB (69312525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaa0cfb5ba6d0089c43b1a98087064b22f947b8ceca9501ea655d8941070c436`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 609.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dca56d6109978bb6ac704538cb9fcc74df9a482314c46d5e965706187626b13`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:95d0c320e6d6f50bd12c4b76d67e966195dba37ee017a76c720c81538b66866e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9676ef442d26ba75cfa34a334afdc72eda6f0079fafbddcdbf02f4f73c2f132`

```dockerfile
```

-	Layers:
	-	`sha256:592b66d4b1d0a8e109407e43fadfdde3f20bd70751027f8d3a6cfd5d4ca50248`  
		Last Modified: Tue, 07 Jan 2025 02:29:37 GMT  
		Size: 4.9 MB (4916367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:794e9f1f8ddfc2b74433a149bc5ee516c2776f8368047410796bb85758c38b36`  
		Last Modified: Tue, 07 Jan 2025 02:29:36 GMT  
		Size: 16.6 KB (16575 bytes)  
		MIME: application/vnd.in-toto+json
