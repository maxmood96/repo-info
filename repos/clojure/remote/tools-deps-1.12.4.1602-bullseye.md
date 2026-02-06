## `clojure:tools-deps-1.12.4.1602-bullseye`

```console
$ docker pull clojure@sha256:947b852320640c1716f935db09f66948d02bc1b02a88abb21cc76a2605ecd100
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:0cb1f4cae1e479c4bdc4e582c795710366ed1a28d24d303373365b2554db44cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215555194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:752de855c91eb8d2ba1185b17aacbb55d87a1769f7a865526a32f0ac3107a880`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:07:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:07:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:07:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:07:31 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:07:31 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:07:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:07:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:07:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:07:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:07:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4837b8a287e31893a57c67e4e7e49ea3681edb8424480549d8b5f5b29691313e`  
		Last Modified: Tue, 03 Feb 2026 01:13:50 GMT  
		Size: 53.8 MB (53756259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c92858be8554371333c98873c16df056b7de4306d2cf737c061a2703742d53d0`  
		Last Modified: Thu, 05 Feb 2026 23:08:07 GMT  
		Size: 92.3 MB (92256235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917b15dffd0f61dcc97930dd75b93d17c87f59ef66e9ae99cc7d2650d32d4110`  
		Last Modified: Thu, 05 Feb 2026 23:08:07 GMT  
		Size: 69.5 MB (69541657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f87207618d85c5a9a09a52d08f428d0fcfed0df12277c4a1a8f7d54c2904c0`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c96a5198031a6fb5218f7dde12a3f02ba29c177e1d0420b087776150dc24c6`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4f86276e6c8f161e313d642754dc791e05b81a8c6c6ab8129d4e3a6f03831b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7382240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a2e27a4744b2eeb1aa114562bda90924fdbd912d3c72f1de7f0a40ba0cd0a0e`

```dockerfile
```

-	Layers:
	-	`sha256:2eeb4cbea33171e472a1b1316dfd932d862176f52b04015d0751ca05c7cbea98`  
		Last Modified: Thu, 05 Feb 2026 23:08:04 GMT  
		Size: 7.4 MB (7365794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b52525e64ddb7d593a820468c9f2cac2f322bb60221e8ecd4d5fca913ec17b54`  
		Last Modified: Thu, 05 Feb 2026 23:08:03 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1602-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:722c608f1728b4e945580209c70e7beeaa1c9d1d08c9f8d0d828e8b85236e328
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.2 MB (213240599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192549e7a783b7ff6665382aca35582d4a07a014536b0fab4a85019fb051085c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1769990400'
# Thu, 05 Feb 2026 23:08:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 05 Feb 2026 23:08:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 05 Feb 2026 23:08:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 05 Feb 2026 23:08:45 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Thu, 05 Feb 2026 23:08:45 GMT
WORKDIR /tmp
# Thu, 05 Feb 2026 23:08:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 05 Feb 2026 23:08:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 05 Feb 2026 23:08:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 05 Feb 2026 23:08:59 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 05 Feb 2026 23:08:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0742c20cdb1eb0c212cefb0ff441553e29e6ccfa92b808cca3d7e8548a6fd569`  
		Last Modified: Tue, 03 Feb 2026 01:13:54 GMT  
		Size: 52.3 MB (52258320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3696fcbadab7bbde16dd9f488e7b1c02faabb92b8e94c7b7232083a6712ceab`  
		Last Modified: Thu, 05 Feb 2026 23:09:22 GMT  
		Size: 91.3 MB (91288273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a9ab8266ce12d92c806736d933ad47c6e48051385bbd7231f1974888b7855f`  
		Last Modified: Thu, 05 Feb 2026 23:09:22 GMT  
		Size: 69.7 MB (69692961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d6276e06ec0da933af9198019852ddbee4d0d55c39bcb756696d213cc62b83`  
		Last Modified: Thu, 05 Feb 2026 23:09:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e704f90252394b671e917a89b6e88a1f1513fbaf4410f740e462c3bb2cedaec`  
		Last Modified: Thu, 05 Feb 2026 23:09:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1602-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:52ced86d2f82e2208c196685a111025b497240121a252187c46b383906b90d80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7387503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f37ce44e2aad0ba921674c626212ef1bacee3632067ffe334f31d5e078fc262`

```dockerfile
```

-	Layers:
	-	`sha256:f65dd3ce85820c8ce8743a2be63b2ee93d66e6fad34243e56b35a4fe919e3d73`  
		Last Modified: Thu, 05 Feb 2026 23:09:19 GMT  
		Size: 7.4 MB (7370914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:551904a45bfaec969a848c59a06893425b563e0a2b64aa0cdbbf8672b1073f71`  
		Last Modified: Thu, 05 Feb 2026 23:09:19 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
