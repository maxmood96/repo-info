## `clojure:tools-deps-1.12.4.1582-trixie`

```console
$ docker pull clojure@sha256:b481ba758feffd6b583e364fc839d427d9a1e7beb3c8aff2ae6103b719293e51
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:9d9a2c784e5a2f27fcafa495e4f3562585761528619e46092c43e5393a3f1a3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.9 MB (226878598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3869f83add22a76d96807db6b0cdf2cf0026c3df81e6bfa7744608e02fa4ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:46 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:46 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:41:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:41:04 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:41:04 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:41:04 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:41:04 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2981f7e8980b9f4b6605026e1c5f99b4971ebba15f626e46904554de09f324f4`  
		Last Modified: Mon, 08 Dec 2025 22:17:46 GMT  
		Size: 49.3 MB (49289520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7194f2d6e4529d76056a69b6d91d6462d56ab855055ea437d17dd36ae6b53064`  
		Last Modified: Thu, 11 Dec 2025 22:41:38 GMT  
		Size: 92.0 MB (92045295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e24926fd1c6b1e9810cc12f91886613737d0232f14a389f0d85fdd1377b8da`  
		Last Modified: Thu, 11 Dec 2025 22:41:39 GMT  
		Size: 85.5 MB (85542745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8bb20f51090c2870abe71a44e8b9ad6057c9b0eebdc324f3868621bafc6883`  
		Last Modified: Thu, 11 Dec 2025 22:41:32 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a07fac2bb02e64d6dd29bf999a97543675fac03780686b1d20e565be2d5bd6d`  
		Last Modified: Thu, 11 Dec 2025 22:41:32 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:69b859e682291e6af1394aaca3b943d8e1ae1a70ef47c870f41959497c1666fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7434676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6156f5da6999c1c8a4593a0c8e44eca58623aa270e5c68e6ca4a6b5382eb0209`

```dockerfile
```

-	Layers:
	-	`sha256:523fcd0747b5aad0f985f08443832eb2ba7d898b2e233de2a71e95be5def3e50`  
		Last Modified: Fri, 12 Dec 2025 01:45:25 GMT  
		Size: 7.4 MB (7418261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6524edd658d84cc24df60fda8e6af3e0cf6aa7cfe8a810296f38973b36d83a80`  
		Last Modified: Fri, 12 Dec 2025 01:45:26 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1abf597a4a92cbc7fb0be4f61887f1b4bf2ea9e72c98747fbfa389f7f4454f83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.1 MB (226064907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c938c9c2044e61144f17817d9834f312f3b78eb2136dc5555750a30774d7975f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:40:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:40:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:40:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:40:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:40:49 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:41:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:41:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:41:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:41:08 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:41:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a828f739420ec96bad6123094a07f3f234998f6cf772e34e0ba733aa8e2b347`  
		Last Modified: Mon, 08 Dec 2025 22:17:28 GMT  
		Size: 49.7 MB (49650226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f8bf036f4bb662531f9f8ea56dbe32e3908b9a17c3510c21afab8ee6f02b85`  
		Last Modified: Thu, 11 Dec 2025 22:41:41 GMT  
		Size: 91.1 MB (91052481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b1d033ad1c35f6d1ac9ba874847b66f1f0e9472ad0a252bced3ccd5ccd1aa8`  
		Last Modified: Thu, 11 Dec 2025 22:41:42 GMT  
		Size: 85.4 MB (85361157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec80d516283b45dda16cf6ce3c9663f3dc7269c7fe31fd17d2497ae4a58ab18`  
		Last Modified: Thu, 11 Dec 2025 22:41:36 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b9a3a462b3d4d8163d8709664d614ec76273a4b95335774a4cc6028bdf951b8`  
		Last Modified: Thu, 11 Dec 2025 22:41:36 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8f56b2e0f2c5d77a2788ee4a00b17af064b3d98cc3ed733ac07e5701ab0a49ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7441869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b38eabae69cc726728553486da4f2526c71c67f9e72400440457c2a74c4985`

```dockerfile
```

-	Layers:
	-	`sha256:d612f6fff36d30e5d456610c4dc4e43774b9bb907dab799d18b0d070f054c11f`  
		Last Modified: Fri, 12 Dec 2025 01:45:32 GMT  
		Size: 7.4 MB (7425312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4322229266bb5499c63ae6c04a31a9b32c6c304e0b4f751e4ee8ab1133b971`  
		Last Modified: Fri, 12 Dec 2025 01:45:33 GMT  
		Size: 16.6 KB (16557 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:0351337d6b303ad2fbe1c9e929e9b70ceb517703213d57a6d529e01ef096d2e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.7 MB (235665453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e710f000b02c1182a81e1d883399552196513d68c1aecc1e067b54154d2c04ab`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 23:32:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 08 Dec 2025 23:32:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 08 Dec 2025 23:32:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 23:32:22 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Mon, 08 Dec 2025 23:32:23 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 23:07:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 23:07:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb00391cdf4b5dc5fe2e67e0bee3770076e9af9efed48ba15cb306902e36c78c`  
		Last Modified: Mon, 08 Dec 2025 22:52:23 GMT  
		Size: 53.1 MB (53108478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe3513d576a2d4d2badd58f02126058233abf53aea816262c3b7f313a199d32`  
		Last Modified: Mon, 08 Dec 2025 23:34:05 GMT  
		Size: 91.6 MB (91610745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da45ec45f7fa7a8009cd6ce07a814e88d0a24ee721dff3402b8b92096674114`  
		Last Modified: Thu, 11 Dec 2025 23:08:46 GMT  
		Size: 90.9 MB (90945188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75068561fd075272328e2d624a007a2b3aef2d0c6c62a8dd531ae2ba505822b7`  
		Last Modified: Thu, 11 Dec 2025 23:08:41 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5df7221d03aa3e1893c77972de57363465493db030f2b83f4e6bed9f355fb2`  
		Last Modified: Thu, 11 Dec 2025 23:08:41 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3517fb2180be464df32a80ee194d1083d31038f33b21dd4e8184760dd137be66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7440465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dabf913b9543056e283f4ec64ae6af5d9e08f4662f2f45e8399c215ef1c7704`

```dockerfile
```

-	Layers:
	-	`sha256:55282e42f7bb304ee79c05e2e1c58d79f7f2e06be32c7129201808c7aaab5ad9`  
		Last Modified: Fri, 12 Dec 2025 01:45:40 GMT  
		Size: 7.4 MB (7423990 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f38cdf47e6dcee61dc3b14357c679c38edd02984bb8e6219feb7d1153988035`  
		Last Modified: Fri, 12 Dec 2025 01:45:41 GMT  
		Size: 16.5 KB (16475 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.4.1582-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:26550c691b8fa8d151856de241a84bb8df27595f4650701290c98c8b05cd51bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.1 MB (224065309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb17aae78e00fc67bb24768ee0725ba897a7b52ea65b42aeaaf2602170e6f68`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Thu, 11 Dec 2025 22:37:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:37:25 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:37:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:37:25 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:37:25 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:37:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Dec 2025 22:37:42 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Dec 2025 22:37:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3f8967bef2f6a8ec916f7d3a0d528a6724093176621c5758addeeece50e41dec`  
		Last Modified: Mon, 08 Dec 2025 22:16:15 GMT  
		Size: 49.3 MB (49345908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1aea96d74749c960c1f1090f28c52cb64429f8a769bcf18dd21864d5a82ea95`  
		Last Modified: Thu, 11 Dec 2025 22:38:21 GMT  
		Size: 88.2 MB (88210741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0219b4a9c3bcdc5421deece773209ab1a06a22a8bf39e1fde71b2153702d42f4`  
		Last Modified: Thu, 11 Dec 2025 22:38:24 GMT  
		Size: 86.5 MB (86507618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456d25c866039a7cbe80116eabc20f7f4119cb1ecd618b74c6e6b568a3c502f0`  
		Last Modified: Thu, 11 Dec 2025 22:38:16 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8973d8890d8771d7f739ac471390920e9f4064b3ea1d7d3039c9567fa95a1f`  
		Last Modified: Thu, 11 Dec 2025 22:38:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.4.1582-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:759bdfe0112260c6619f72702395bef44dcc1e98170d3727f65255f2441f980f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7433146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09b623dfdab4f63e1ba0f2626a908cc03d68cf6fe0190e7151dc346aca07fdbb`

```dockerfile
```

-	Layers:
	-	`sha256:0d5389051a13dcf8da5a378369c0fcc874698dfe5295363843d82ea9a696a68c`  
		Last Modified: Fri, 12 Dec 2025 01:45:48 GMT  
		Size: 7.4 MB (7416731 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd96911c650bf5a9700916a5a52e2bf4a2ba2119e9e418cb2a1450b1e664c535`  
		Last Modified: Fri, 12 Dec 2025 01:45:48 GMT  
		Size: 16.4 KB (16415 bytes)  
		MIME: application/vnd.in-toto+json
