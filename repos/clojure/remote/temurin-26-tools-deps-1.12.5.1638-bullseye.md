## `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye`

```console
$ docker pull clojure@sha256:2a25b603aa36e2640ae229fa94f320fd2a3e786aaf6281b467899baf3bf2a636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:b1d9fd1eb298c43919b7be8fddb9a1f3db5360607612a3be0a6fce754cc52f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217844297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f3b69915112ba86ca9bafa3d844312e4fe3a189a9dd46cd62d8b59821d6c85`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:36:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:54 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:54 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:09 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:09 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:09 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:09 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc479fc0384a7d61f2e05cf29fcb9d03c7b177e0045a3bbd6a4648656280f7c`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 94.5 MB (94455680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6b760a9982992c9dccec36c824f6d7efbd179cc7da84f878508ca03e14481e`  
		Last Modified: Thu, 14 May 2026 23:37:31 GMT  
		Size: 69.6 MB (69624228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63828bf314a366cbc5387a4e15478bc9174fd74f4a003909546206d7de9d1502`  
		Last Modified: Thu, 14 May 2026 23:37:28 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b7e30bd2ba8e81f43f9d5396ee4ab536916fdb7c5210a03dda22b0ca36b24`  
		Last Modified: Thu, 14 May 2026 23:37:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:206292cd78f014145e4967d471acd91c8ba079640a3f7f39832b903c1376f85b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84b3ea4c4974e89d278c72db657afcfd70d6a82ebcba48db86273c29d2e0022`

```dockerfile
```

-	Layers:
	-	`sha256:88a6be56d3fc34c5161fbab70c7cdac6d42c2b0a514ba1e0aa289c9e58813ebb`  
		Last Modified: Thu, 14 May 2026 23:37:28 GMT  
		Size: 7.4 MB (7373155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31f7266fbfa80efac37ac808f8534306bf0c48f6219bb751c42a4b210da6cc8f`  
		Last Modified: Thu, 14 May 2026 23:37:28 GMT  
		Size: 15.8 KB (15771 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9b4e6e40f8afcc16f9981f8ce33b06e6683510b19187a58674116c984caa1e92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215413697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d2769d29ef12cf801f568b0077af78d580ac76720c10e15e2f347427367889`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:37:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:37:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:37:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:37:01 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:37:01 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:37:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:37:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:37:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:37:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:37:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ee90f933e4f1c558355252a405045e46a004872aa3e2945c3e184beec7d5f5`  
		Last Modified: Thu, 14 May 2026 23:37:36 GMT  
		Size: 93.4 MB (93395200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfd83f95e6abb8ce09edc23d17d9041d28802dd41bd7ec5a428c23bdcaa93e2`  
		Last Modified: Thu, 14 May 2026 23:37:36 GMT  
		Size: 69.8 MB (69764243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4df78cc47b10365f7dace4c666b18eefeec779dae8e5a280634c78da947eed`  
		Last Modified: Thu, 14 May 2026 23:37:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ff774e68bf3802d24fe7cef09bf9958da90d7b2904854653faa0574ca2721`  
		Last Modified: Thu, 14 May 2026 23:37:33 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-1.12.5.1638-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2eb5007739d73fa8740e5233fac77580999efc0ccc0ded73c1b97cfe99b63c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0206ad7f08547f761ce7ba8a6620191701e01b16b62535b85d39c7db2548f45`

```dockerfile
```

-	Layers:
	-	`sha256:b3da7620da741e85abc4df48c61814387dd8ea98e8102c430e72718c04af3d1a`  
		Last Modified: Thu, 14 May 2026 23:37:33 GMT  
		Size: 7.4 MB (7378251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:756e5d02b246908ac71cbbc2cf43a45fadd248ec346de5fb56bf487c8f67bf8b`  
		Last Modified: Thu, 14 May 2026 23:37:32 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json
