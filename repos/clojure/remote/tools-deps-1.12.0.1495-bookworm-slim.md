## `clojure:tools-deps-1.12.0.1495-bookworm-slim`

```console
$ docker pull clojure@sha256:407b243598d6a2260c59bbde28a6b752163114e033912ce52af79d69ad3d1057
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1495-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:781fc1c15cc5b84efb500130ec52ec939b0051a8ddfb82728e22fd07faa641ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.3 MB (255308534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:953e808b42346f879eeb550c208fda6c5f6615f86a09bb7956beeb83a21008a0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2176b2d01f419bbd22117d470d594e2ac21fe2d96f731aa22f80eb1458e63fbe`  
		Last Modified: Wed, 22 Jan 2025 19:37:11 GMT  
		Size: 157.6 MB (157568693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99fd4a87b44648fc148304030853a2bee5abfb855d260f7bddbfb258f546c5c`  
		Last Modified: Wed, 22 Jan 2025 19:37:10 GMT  
		Size: 69.5 MB (69526384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:450126d20d11d3a05a30648dd233ff8ced85e436b768e6bedec026b29862f43b`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3bbdb64ec2a03c9f79335d4e69eee1e71f6fae247d7867bf7a4366ab6a757b`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c3c6471941fd58e438ea501246c78752559e4a2996216a763250383e3d31f2e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4932941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163ad32c60ea8c38e28d57d8056859cf00575f11995c88e967fc435fa601727d`

```dockerfile
```

-	Layers:
	-	`sha256:e94fd0caf55c1743e1c6f53fd66faf9725e5c5b4e958065e4ad9f404a93ea6c1`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 4.9 MB (4916367 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78b0aa2851e4809a5a93dbe69991dc922f8283fa764018b7a508aa5229b43dca`  
		Last Modified: Wed, 22 Jan 2025 19:37:09 GMT  
		Size: 16.6 KB (16574 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1495-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:04badd2141f3e6f7e2af194861d05f3968072e365526191464d5e1d64b188f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253209308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0428705555083120ef4a7e64420ec1d9fbd910493a522d2d6a795719eaffa6f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0003aa2eca93752532c4a7952a26415d34e92059ff3c5e2dcb9bec0f8bce5bd8`  
		Last Modified: Tue, 14 Jan 2025 12:33:47 GMT  
		Size: 155.8 MB (155793151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f25b1c6036c62805f71d4a73abb6dd3ef918faf8db10900f639947f74b24a7b`  
		Last Modified: Tue, 14 Jan 2025 12:36:27 GMT  
		Size: 69.4 MB (69374086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f8d793546d40dcb8f56497f693aa5559fff474583524551e0d1d4e30e23aca`  
		Last Modified: Tue, 14 Jan 2025 12:36:24 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991af16a9ec258e64c5376a06aee1775c2862e77b5e2ae6cfc305f1391061dcd`  
		Last Modified: Tue, 14 Jan 2025 12:36:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1495-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:34a06d18d00cef35031f5f3273362765c658551dd2bbbf3a80ff1f788349a459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d1c00370cc2ab5796822f240561b1452c5073aeb05e7e0730e1c034dcc740ed`

```dockerfile
```

-	Layers:
	-	`sha256:dbf62951b6aaca2d188882e719f9eb1d732a4633104efaa6ad090604c25fe06e`  
		Last Modified: Tue, 14 Jan 2025 12:36:24 GMT  
		Size: 4.9 MB (4922152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ab9d09e15bdca748ad57255e83fb31290f66ecf0876e05a5f9a2c6d24baa18`  
		Last Modified: Tue, 14 Jan 2025 12:36:24 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
