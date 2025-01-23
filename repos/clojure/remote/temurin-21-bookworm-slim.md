## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:fe68c87f117556082ca16927076578497aabd7fd40de222cb8a0194f75687b0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bookworm-slim` - linux; amd64

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

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:3e05d315e9b4bd98bd7f76ad21622d02a16f68339869f61622589faa0b7dd0de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 MB (253209365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc38a4a09d47f7b8708e4ce7dba9e2eaf804566341673ebe7c99712d6f2cc80`
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
	-	`sha256:1e2b2cbcec988c950b61c68558a29d15b455bb56c17644373d901a2c20f07fa0`  
		Last Modified: Thu, 23 Jan 2025 02:54:30 GMT  
		Size: 155.8 MB (155793069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a0bd9eb86333085b23e0df46bf51fff6f672871ecae09cf3398dac3c25ee7f3`  
		Last Modified: Thu, 23 Jan 2025 02:59:36 GMT  
		Size: 69.4 MB (69374223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba639283a1925c65bf15224c462ac80ee81533272cdba7f002cb303ad1dabd8`  
		Last Modified: Thu, 23 Jan 2025 02:59:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019caf3e9d170ee2d7c923c2d3549d3a644ff767bc7b3b35cf1a976f45f96f85`  
		Last Modified: Thu, 23 Jan 2025 02:59:33 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:808772e6162652afae7025651099e6a597c723335472c1dca606dfd89ce4f816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4938869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b18bfe4e68b6a80551fad024c9f8e3da3bbd6d3966ba171db7e97233dbddb9`

```dockerfile
```

-	Layers:
	-	`sha256:1e7ad333b12a0ee51274e82b1e4a4f94317795f104ede21bdfa6a7f3d4dc8acf`  
		Last Modified: Thu, 23 Jan 2025 02:59:33 GMT  
		Size: 4.9 MB (4922152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a47525ed30444dd492be6a7c7fe47e6f69648d7e6ac7b1ecc13eb55870e7db6`  
		Last Modified: Thu, 23 Jan 2025 02:59:33 GMT  
		Size: 16.7 KB (16717 bytes)  
		MIME: application/vnd.in-toto+json
