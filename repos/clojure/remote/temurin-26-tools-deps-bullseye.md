## `clojure:temurin-26-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:67df4173ab9cb0c8698e0133dde303141c8b543a745e34f092a6b46b5c1c2b61
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-26-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-26-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:09ae6085a8915ea6da20a05395c4e8cd0ff34d8d9a33a42882098241609c61c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215379919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce62618d488a91f1a59cbbe11ae0853e14cd774be45b19a7a62af27f80ba8056`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:19:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:19:45 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:19:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:19:45 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:19:45 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:20:00 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:20:00 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:20:00 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:20:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:20:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad153cb26a39ff9879f51336e2573a4bfb5963a61a28bd4be69525edd0e761e`  
		Last Modified: Wed, 15 Apr 2026 22:20:24 GMT  
		Size: 93.4 MB (93395204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af8e6db806e0c8465faaa756dc593c3749e9e07bd2e79fdcc555ca2edf3a3470`  
		Last Modified: Wed, 15 Apr 2026 22:20:23 GMT  
		Size: 69.7 MB (69736058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a65e93f137f9f31acb0192c122437a0c4c22369e6d93ff43e664b24255d1f5b4`  
		Last Modified: Wed, 15 Apr 2026 22:20:20 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297e2027492a7468e39092e26f988a8195f2c3872fddc7eff282b0a6f3b69f3a`  
		Last Modified: Wed, 15 Apr 2026 22:20:20 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-26-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e08fc7a988f064bba8c7486b0b94234461e41d8ce49fa597ff4144e5abcae130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b81cf7866ecfd7bd0ec4e830690eb8467b105c867248407d255a600f48802a`

```dockerfile
```

-	Layers:
	-	`sha256:3ffaa4d3bdfb6e83832ddce5932eaa47a12393441bc4ad81ab5cf1bb0c6ee6c2`  
		Last Modified: Wed, 15 Apr 2026 22:20:20 GMT  
		Size: 7.4 MB (7378253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25acd9aa7e4c10df0428446b34729ca9d890a398152d626b661a5190ce866452`  
		Last Modified: Wed, 15 Apr 2026 22:20:20 GMT  
		Size: 15.9 KB (15888 bytes)  
		MIME: application/vnd.in-toto+json
