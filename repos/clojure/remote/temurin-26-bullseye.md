## `clojure:temurin-26-bullseye`

```console
$ docker pull clojure@sha256:4fa1f376585dd2714e3878cf2558403bc89c4c42e5c73050f977110acb8201b3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:bd463fca99809324e308f14b672e836bf32111d56b62a1faa3a8e8bb3ef60f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.8 MB (217820476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c817b3e8df9a4b987c42aaa2bf2e1d49a9fb48e016216b4e3bda003c6d5f09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:07:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:07:53 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:07:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:07:53 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:07:53 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:08:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:08:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:08:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:08:07 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:08:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efe03c33c6a9343a3dec7778e25eae65f4aaafd2176d98dbf0c245ad2329bb1`  
		Last Modified: Wed, 15 Apr 2026 22:08:31 GMT  
		Size: 94.5 MB (94455697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8192e7bc1e7173ca55efd53ab0b22320c5958e7674fae6f1b543eeef6c9e1667`  
		Last Modified: Wed, 15 Apr 2026 22:08:32 GMT  
		Size: 69.6 MB (69600944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2639735f58c6a27ff2762638d31875b4a11400497375bb7bbcd1939ff65a62b`  
		Last Modified: Wed, 15 Apr 2026 22:08:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155391f3400eceef12cdb81ce90a51c168bcff3d6d7d8646e62ecffe51196a0`  
		Last Modified: Wed, 15 Apr 2026 22:08:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2ab2f8da3a4c3f97ed7363e9cd842ac1ab5a18d22df104fa31e5095c8ba94863
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7388926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06ed17e458050bffa0cb5290c95bfe1886ca0dc021e24a27e20840e111791c3e`

```dockerfile
```

-	Layers:
	-	`sha256:e89d193479df8e6e62d79d19c80a0c9e0030789a7b2486a57a6d0659f7b62bde`  
		Last Modified: Wed, 15 Apr 2026 22:08:29 GMT  
		Size: 7.4 MB (7373157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fec70d3ecf017bb81bc78f241be38b113cc988a3882c4a8df01035bde298bb6`  
		Last Modified: Wed, 15 Apr 2026 22:08:28 GMT  
		Size: 15.8 KB (15769 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-26-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5bf7847b434a2276080c4100f6a9789a159a1f7c28ba2ff2badb3e560da184c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215372378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c11d8b7d24a1bc3df74183c0e630175c06d329b903636692f4fecad548e3f21f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Thu, 09 Apr 2026 23:36:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Apr 2026 23:36:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 09 Apr 2026 23:36:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 23:36:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Thu, 09 Apr 2026 23:36:57 GMT
WORKDIR /tmp
# Thu, 09 Apr 2026 23:37:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 09 Apr 2026 23:37:11 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Apr 2026 23:37:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f9ef63687cdd1afbb2cb3db99b44a750832b949f7f5ae115b6905380c3e240`  
		Last Modified: Thu, 09 Apr 2026 23:37:34 GMT  
		Size: 93.4 MB (93395164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2b94857667fbe237a25bfd9915f7e939dfb0bae05b24d346cf71ffa469dc72`  
		Last Modified: Thu, 09 Apr 2026 23:37:33 GMT  
		Size: 69.7 MB (69728555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76025c2a834d9f19caa92ba4cba5ac755e4691d36ef2df9d739c31cff7415913`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c664159c4f21b3c629693818842e9ae46286ed77810e8e3f583aa94502d5e7fc`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:d0d8be824316c0a14abbccb5601db8f8eea76d8ab4275e0fa435c372f9ce226e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5aa3d7ddf38c1336f29fed6ee80da14c90cdb7806c31cc9fdd3f6199b56cd161`

```dockerfile
```

-	Layers:
	-	`sha256:e08b06ebace33a0d73e5f78c1e93f36762c4f8fcfafc8409bd465240f8d50f1e`  
		Last Modified: Thu, 09 Apr 2026 23:37:30 GMT  
		Size: 7.4 MB (7378253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19e9d3a0df83ab135733f38fd3c32f3ce8ff713d46039169157243227768d705`  
		Last Modified: Thu, 09 Apr 2026 23:37:29 GMT  
		Size: 15.9 KB (15889 bytes)  
		MIME: application/vnd.in-toto+json
