## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:e45f2dc223a1af6b68974d0a8a4d0d8d43819233b85b6f23ff803e286fce07b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b894c3a98ec64091a09a0647104207d255a78702f06a83f52344038279eecfe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234257345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3995fa80891ef0d5d94537dc7c9bb2a8c53da12eadb04d31de9331f62e3d7fcd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:55:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:55:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:55:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:55:31 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:55:32 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:55:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:55:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:55:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:55:45 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:55:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd1b97a95a10ded4767bfcdbb3d042b961d107d141121fdbb255239f0ca115f4`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 30.3 MB (30258497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2577169c8fc5d1bf69fc3fe7813de9e39810973195e0adaf02fe17a399f89632`  
		Last Modified: Sat, 17 Jan 2026 12:54:00 GMT  
		Size: 144.8 MB (144847942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203172d7f597c671b5fc94dc9913bdec9a04682dc73274882527a13cc58f5833`  
		Last Modified: Fri, 16 Jan 2026 01:56:04 GMT  
		Size: 59.1 MB (59149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd1b9ba6447b927b6941ebd6461ee7babc992f2afa95261c8333813b7623b1c5`  
		Last Modified: Fri, 16 Jan 2026 01:56:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea5ca12b30c18c82c64eb484ccfafa39727fea022a0af8d8b12f7c09243b513`  
		Last Modified: Fri, 16 Jan 2026 01:56:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:f74cb75e98b4608019108521cec2643f77afc2559a87711da447ee016dec1eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5323905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f1b5eea12373f68872ad499eaacbaf5d79854d38ae4cca68a664ccae6f1b503`

```dockerfile
```

-	Layers:
	-	`sha256:fb3f50d17e03c1a611ad0f914cc2714844241cf025d5aed1f47acd00c83d93fa`  
		Last Modified: Fri, 16 Jan 2026 01:56:02 GMT  
		Size: 5.3 MB (5308069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ceff3496108a9a9fe5726e2f5059425aeb6ecf2c0d4b96827bc848435f2e481`  
		Last Modified: Fri, 16 Jan 2026 04:41:09 GMT  
		Size: 15.8 KB (15836 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5013acab1b10ed27db10fa1d57c83b70f2552d3a1ad21755278d46755701829a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231713274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f194b8915f910ee3754a34d52dacd5681e291b97768d1fb2ae025eebda5031f0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1768176000'
# Fri, 16 Jan 2026 01:59:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 16 Jan 2026 01:59:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 16 Jan 2026 01:59:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 16 Jan 2026 01:59:18 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Fri, 16 Jan 2026 01:59:18 GMT
WORKDIR /tmp
# Fri, 16 Jan 2026 01:59:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 16 Jan 2026 01:59:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 16 Jan 2026 01:59:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 16 Jan 2026 01:59:32 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 16 Jan 2026 01:59:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7781088accb552d6473ed64f4649a64684d928b7cfad973d13e5c50942bf7a5b`  
		Last Modified: Tue, 13 Jan 2026 00:41:59 GMT  
		Size: 28.7 MB (28748518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7718adea1b9082ecf28fdb9d8ec237241806bde5e7d48a42e09eb8564f3818d7`  
		Last Modified: Fri, 16 Jan 2026 02:00:18 GMT  
		Size: 143.7 MB (143679931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b7a994ace7295260d2ce8e67a37655b4f4e1fe846aee7a8f3767c8e01fc9394`  
		Last Modified: Fri, 16 Jan 2026 01:59:55 GMT  
		Size: 59.3 MB (59283782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07add196ec7d46a90523fa60208a9697bd8595d94eeab9250026726c1239e470`  
		Last Modified: Fri, 16 Jan 2026 01:59:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe990075a5b7b6e01c2f0154bffeddac158ba124798fc65c9be8a9d55b822149`  
		Last Modified: Fri, 16 Jan 2026 02:00:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:aeb5b3da34908dccb521cfd30e7288bac15180c7388ac8b90139cbdf438bd7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fd60a9f0ec828ce5aff4045c01e17db050f9aa7f26c952d5bf46b2ec85e45d`

```dockerfile
```

-	Layers:
	-	`sha256:39d8e6d76add81cf69c5f0966127376dbcb589007b7c2a1bc10ee62ebecfce1d`  
		Last Modified: Fri, 16 Jan 2026 01:59:53 GMT  
		Size: 5.3 MB (5313801 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11f90853eba34bc8e1b5b92513b19d563370c5fe03be23377a64b48fa2b3f94d`  
		Last Modified: Fri, 16 Jan 2026 01:59:52 GMT  
		Size: 16.0 KB (15953 bytes)  
		MIME: application/vnd.in-toto+json
