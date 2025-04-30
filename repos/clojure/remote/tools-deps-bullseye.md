## `clojure:tools-deps-bullseye`

```console
$ docker pull clojure@sha256:afe720ac9ab26d6dfd3a2cca38422e7529878e82d0764b283a4a55a1880026ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:59ff9fb550215e84b3e394fad0d0f0ae8e3eef2ba7ef2d78c96fcac70ca82e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.8 MB (280778521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e262f19910b2a932cc917001a43bf7216890b452a5b51f5a614ae7823dc79a78`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd86af4d1b05b1024b612c413f592bf053601f5b3d6d0f31d9842e33929b116`  
		Last Modified: Mon, 28 Apr 2025 22:08:08 GMT  
		Size: 157.6 MB (157634490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556f5c0e46f16e554d9766549a4e0fbfb3c625a36bb1ff4ce624665f5735ee81`  
		Last Modified: Mon, 28 Apr 2025 22:08:07 GMT  
		Size: 69.4 MB (69395250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1251b964e9796522eae64ee2d591b7ec132fc3f105f36e9010c3f3cecc3bf083`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bce1c5f25602ee233f19989ce58aac8ada729dc5f78464711e47bf8e0a2197a`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:30cc313e51e86b6b4442785df13ae966f5b96b3dad861492b430a1ed7b2294d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7226829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a34816568e06373d0755d17e75823146f0261763f81c18e1eddab106a63d7ef`

```dockerfile
```

-	Layers:
	-	`sha256:591615c195268730dd69372ea004dad60dcad8904f59070e516574e36a13362d`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 7.2 MB (7210333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c1ceffc6ecca3bb9cf2b4544997715b2da2525d0196e5ac034c3b6ca3624400f`  
		Last Modified: Mon, 28 Apr 2025 22:08:06 GMT  
		Size: 16.5 KB (16496 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ce72cf9340f0355dab310428b1b4ebee37cc88593da095105369f8391299f0e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277705241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb5e1d52e4983669ec5b04351b73d93d59c727fbabd70e1e0a8804da9d4904f3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Mon, 28 Apr 2025 17:24:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Apr 2025 17:24:54 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Apr 2025 17:24:54 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Mon, 28 Apr 2025 17:24:54 GMT
WORKDIR /tmp
# Mon, 28 Apr 2025 17:24:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 28 Apr 2025 17:24:54 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Apr 2025 17:24:54 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Mon, 28 Apr 2025 21:20:53 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61c157ab8eb81c07fbfae63cd9fe879f3c276295291ce0524b491f7a359eb662`  
		Last Modified: Wed, 30 Apr 2025 01:46:35 GMT  
		Size: 155.9 MB (155928834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13506fe2d6b2ce347edd3ab615a7bd796a465f1e3d60da021f0acf8f602c673e`  
		Last Modified: Wed, 30 Apr 2025 01:46:33 GMT  
		Size: 69.5 MB (69529389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4e74d14199dd011282c596a864ad8576b2f9edb40fb804e97b1a5d6e58118a`  
		Last Modified: Wed, 30 Apr 2025 01:46:31 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0678d31f455b7f7b6bd02121b70371c5a7d3b38fc718a04f40c3d2b9584139e3`  
		Last Modified: Wed, 30 Apr 2025 01:46:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:dfc9084226f4aad70e461e42b8ab2488e2e1257870562fb7b0d4cd08c7fdf191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7232095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c514468329f6ca7e3039528e2e90bb1abe2db7c53bd3e96567a61d3a41723e`

```dockerfile
```

-	Layers:
	-	`sha256:7eb5f7c775e9f42ea1d88241eceeebb95f41b34a9c2ce96797c1d04673f8e068`  
		Last Modified: Wed, 30 Apr 2025 01:46:32 GMT  
		Size: 7.2 MB (7215456 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c2513c3a840ae918d46707c05c2499276c475cda0c68d0d919bac6d154d716`  
		Last Modified: Wed, 30 Apr 2025 01:46:31 GMT  
		Size: 16.6 KB (16639 bytes)  
		MIME: application/vnd.in-toto+json
