## `clojure:temurin-23-bullseye`

```console
$ docker pull clojure@sha256:d39483cb5fdbc5cc65a2f0d5c104561f3885948b33b3c53a797f60c76e8007be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:8ccd78ad67b069cc194d4a349ab4052d42dd4de3f17eec61270799bfe889a8e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292056789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce84d77a22aee23743a8eebeebdb00950f60685bd3edbd0765fb5c94406eb54`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:603894b180221fc8174e291cd1177a2b9c09a07d1d9ba4d5b5aecdf80ad91fbb in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9439c0e98e5f72dba1ea7cf303c3ca61ff9a91b26911886adb4266e2ad40bb58`  
		Last Modified: Thu, 17 Oct 2024 00:24:16 GMT  
		Size: 55.1 MB (55080611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb4f5a4cc339643ef766a5b1d19f72fc33ea13bbba812cbbc41464d79f2a428`  
		Last Modified: Thu, 24 Oct 2024 01:56:57 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c846d96cb60365f2231623deedcb30f57dbd6684b1105bfc2fba3428bfd9761c`  
		Last Modified: Thu, 24 Oct 2024 01:56:56 GMT  
		Size: 71.7 MB (71680001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0773a969f68a620df69aae1362891deb6f1584916a7cefb0f4b0ebf996d994c`  
		Last Modified: Thu, 24 Oct 2024 01:56:54 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a729d417aefd9dfb81c250627142f3439fb2e2dc6663bc62c6d88725015f449`  
		Last Modified: Thu, 24 Oct 2024 01:56:54 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:373b14d6a3f03dffba4586f37444a2208ad48c8a6c98801e61e85e8c7e8fd62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7236490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bad4f185d7411a62ff0bd2ae905eb320678d37c8c209e30137149c891139c4`

```dockerfile
```

-	Layers:
	-	`sha256:da846d32d159d250e6a2e4f460357caf34412a91b41e60d711001dd55fc2b60c`  
		Last Modified: Thu, 24 Oct 2024 01:56:55 GMT  
		Size: 7.2 MB (7220847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c11c0ebd5e6a5b7112d041f845a13316b826649f3b148d6d3cca78b91d295b7`  
		Last Modified: Thu, 24 Oct 2024 01:56:54 GMT  
		Size: 15.6 KB (15643 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f58d6eb0c91e8ecc82fdb03f8f502f49497d118db79e1069779985e27932308e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286455660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aba2d4b5226671c7095b2ab155dd6093085523e72a6b8641a05d6e77c63ce538`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:bfb52ce9788d517977c9e84dad795a6adb46efc0e8eff88853137b783826c104 in / 
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["bash"]
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:76475c2689e229fac9e8ba4a02e64decb7fd62b2a3e4ad65ba97f8e1a35471f2`  
		Last Modified: Thu, 17 Oct 2024 01:14:55 GMT  
		Size: 53.7 MB (53734895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e3acd407382ba38be4751d630a7d727bf3b7c34f0761ee6972cc6a0d9947b0`  
		Last Modified: Thu, 17 Oct 2024 08:29:57 GMT  
		Size: 163.3 MB (163252799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb74ca72c72562f7df25601c768ceedb917c24fc75e71697f0be9c5fa72a1746`  
		Last Modified: Thu, 17 Oct 2024 08:34:14 GMT  
		Size: 69.5 MB (69466925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6f5cdb7ea85c7b78d28ed4315ca5d3de5b3f202146f830d75c3d4b4508a12d`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8cc0b325b8497bd2ccce895b6000f96e8b8c7e95f6e67adbf877a1e9edb8c1`  
		Last Modified: Thu, 17 Oct 2024 08:34:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:1478a59721d182dafbeb4243dc6ca297cacfe2aa64356761ad907ef4a27b89d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7241068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7ca0d6638452a680b8057195d7b2ea37e86fb6a04c4254f377a2afd0b58a20`

```dockerfile
```

-	Layers:
	-	`sha256:a3916478bffba3e5e3b5ab178bffe403b353f4af49ffb35653214d35927ea683`  
		Last Modified: Sat, 19 Oct 2024 12:23:13 GMT  
		Size: 7.2 MB (7225312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e8fab135e139f3be9266fbcf4585d0251694332cd3ddcc979043498674ae886`  
		Last Modified: Sat, 19 Oct 2024 12:23:13 GMT  
		Size: 15.8 KB (15756 bytes)  
		MIME: application/vnd.in-toto+json
