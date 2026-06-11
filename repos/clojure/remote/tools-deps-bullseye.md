## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:c93188ee85cfbcf965a9e29503ad10fc8391b4566b998f27e35570e2bbcb58bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2253fec40fb8ef22f3c53c4342b6d5eebd05be9277550cb894a5a1237ba7174d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.9 MB (212859310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590ca894c1e6f4c2e540d5d6e612f0e9c8d8ac32fed900e74bdb0e2eeec5cdd3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:21:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:21:01 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:21:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:21:01 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:21:01 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:14 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af48a3e7696e07f88a02f9674e541901b65eadb5cf0f62e566b1d895099a1e9e`  
		Last Modified: Wed, 10 Jun 2026 23:40:09 GMT  
		Size: 53.8 MB (53771769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54ffc41655333922261ebc7615f639e4dd2e79ec161b94e8e92032a8c6fcda34`  
		Last Modified: Thu, 11 Jun 2026 01:21:40 GMT  
		Size: 92.6 MB (92574586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1455c671204989a3028dcf00d4ef5d4eb09c34e02becd7fb95d1627e251cefe3`  
		Last Modified: Thu, 11 Jun 2026 01:21:40 GMT  
		Size: 66.5 MB (66511915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9fde9ef9182f8b709cc80aabc468c6592598fcc6ce63d02e250523274b7c74`  
		Last Modified: Thu, 11 Jun 2026 01:21:36 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1785f49b5c9225f930771bb1212e071325044eaa652e53bcdfa8b9c76771a6`  
		Last Modified: Thu, 11 Jun 2026 01:21:36 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:ec4fbfefa8f38ef5f21de2e43346ef07ec0893351b727460ac3eaa47377108ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7390119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830416cb9e56d9626ceb4b4ee94e0f8349e4a06e568b8f1841d924ce85758c6a`

```dockerfile
```

-	Layers:
	-	`sha256:6b5f396011d81e2ef764319e2fa657b35ee30f03d3ed554311a03e6044ccd75c`  
		Last Modified: Thu, 11 Jun 2026 01:21:36 GMT  
		Size: 7.4 MB (7373519 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a3c5644487741b47f9113bc8355410a9f494ab08465ccd2deac97895c10f17da`  
		Last Modified: Thu, 11 Jun 2026 01:21:36 GMT  
		Size: 16.6 KB (16600 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9aa64e93304e9396d87ac8d258f595ac5653d2b40525645c87efdaeee66e9f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.5 MB (210484887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd71aa9d81699c6dc2deb7c82fd8349eb7564837707d23d46b1a272e3c45f2ac`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1781049600'
# Thu, 11 Jun 2026 01:25:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:07 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:25:07 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:25:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:25:20 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:20 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:20 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7c21e59e753cb91625909251110d6e4cc4a5411b4b7b37f74a62e56b927b7f1e`  
		Last Modified: Wed, 10 Jun 2026 23:39:58 GMT  
		Size: 52.3 MB (52264114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3ef22748e392dc9826bc425bcd4082472c276a6413e0d192c3e0bab2d526ae`  
		Last Modified: Thu, 11 Jun 2026 01:25:42 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2458c285f9d2977977792daddfc6404b9a7a553ec3272958f8b4b4053e58dad7`  
		Last Modified: Thu, 11 Jun 2026 01:25:42 GMT  
		Size: 66.7 MB (66677484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e81c26b3a79cc332dd6a01927af0f7c7bc68e4d5592df71434e5de20d89473`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03f9a719021d1c94fb4e255066d46ff20ce530b09ac1363efa1e9d9b6776dd60`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:8448c280f6089bbb2b184b47e161486d4fe9f8481d30efaa3e3f8908a2c348a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be89e72d6a2ab30106d2a2928822027c885e6b75a5f97904af614b4de16c61cc`

```dockerfile
```

-	Layers:
	-	`sha256:8ce725cfc0fb245647eddaebb056a71f0509ea60f61294e83dac13e9c9fb5f97`  
		Last Modified: Thu, 11 Jun 2026 01:25:39 GMT  
		Size: 7.4 MB (7378639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:013efec93ce4169a0b8767ab35c6b2299dc536170823de4bbdd54ca38b22455a`  
		Last Modified: Thu, 11 Jun 2026 01:25:38 GMT  
		Size: 16.7 KB (16743 bytes)  
		MIME: application/vnd.in-toto+json
