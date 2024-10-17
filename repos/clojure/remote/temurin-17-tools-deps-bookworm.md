## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:f346a60137964f3a1ef75ca36e9265239f3213502ed1bcda7397591126687efc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:9e86d8a38a6a0d3a7bcba2c56149fb7210341bc5cb50bd98330c47f12f51bf76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.7 MB (275650899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa407c30ef19838ded03042ac70b442634eaaf096e584f6113d15b7fb3918b94`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:b4987bca8c4c4c640d6b71dcccfd7172b44771e0f851a47d05c00c2bdcd204f6 in / 
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
	-	`sha256:7d98d813d54f6207a57721008a4081378343ad8f1b2db66c121406019171805b`  
		Last Modified: Thu, 17 Oct 2024 00:23:37 GMT  
		Size: 49.6 MB (49555023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87c9a183a4c67a8e4e1c83f13e814c3db357e5f2b449e5483b511078a3d294d`  
		Last Modified: Thu, 17 Oct 2024 01:13:45 GMT  
		Size: 145.2 MB (145166552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751059abffdf2dbc9f0331621de9842530eef2329b06375906c5904255c529d5`  
		Last Modified: Thu, 17 Oct 2024 01:13:41 GMT  
		Size: 80.9 MB (80928285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725029bbc5f23462e9f81465891b4a802626f09551dd7800038b79accdc687b9`  
		Last Modified: Thu, 17 Oct 2024 01:13:40 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e95d8d1b3849041768e96247497868afb0dde5ae1b9654c0d59ece540428ff`  
		Last Modified: Thu, 17 Oct 2024 01:13:40 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:827754d75b0a65c03513e7f4c787c9d858b83e5d37d7bb084db8013493924964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7171483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03498ccdd13a8623c10d02115378d14086eeab3a12189ee4eb352a8dc1f04f18`

```dockerfile
```

-	Layers:
	-	`sha256:2c0672c4a5e50ec6359ebdba7c7506bd156e16dcf5e2547a3ab96051beaf24b5`  
		Last Modified: Thu, 17 Oct 2024 01:13:40 GMT  
		Size: 7.2 MB (7156006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79c76f1d78f595e5083be4ac1a2a41c66f1f74aade4e3e2d60d88df26bf20be5`  
		Last Modified: Thu, 17 Oct 2024 01:13:39 GMT  
		Size: 15.5 KB (15477 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:320bf0f1c96f0558dad596e0cc903f93c984bb4ab16583589889045a93735d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.3 MB (274335545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3271405a1bdf6c78265d374b6e50fafdd48c4b2b271b0762db28d260df5c4587`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:1df819221542e236e104deb2624ffe4efd79382aed25b3ab20088becaeadad31 in / 
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
	-	`sha256:c1e0ef7b956a07c7b090256aa16cbb0550a34d0625d1d23c5b1a76e92a58d01e`  
		Last Modified: Thu, 17 Oct 2024 01:14:19 GMT  
		Size: 49.6 MB (49584978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af79cbd2bebb502c38437b7b81f3b9697a59e5f45be49cd74b73bdf63f10ac08`  
		Last Modified: Thu, 17 Oct 2024 08:11:33 GMT  
		Size: 144.0 MB (143959476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8e70c0e27f916331f49a283267e3e257bbdf87e572c6f36ce5027dad023c85`  
		Last Modified: Thu, 17 Oct 2024 08:15:51 GMT  
		Size: 80.8 MB (80790050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f3f670afbf9852f5caceb4280e54536843c50f984fe64afd5e4f5dc1bff5ab2`  
		Last Modified: Thu, 17 Oct 2024 08:15:49 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc01a5b0dc85d191e594ef288946e0cde25e66fadaa921e675ebbb4c939e6dc`  
		Last Modified: Thu, 17 Oct 2024 08:15:49 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:9bdae866eae3728f33ab5557871366e3209df9edc39486c02ba4e6f7892abceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7177357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb84bda3159213a82c8a544fc3b2371dbe29dd355b1ddcf35cf8e9759214f43`

```dockerfile
```

-	Layers:
	-	`sha256:c3cf51aef7296fb3b4bc39e303a252ec86f17fdfe890a065e8c2e173a9aa287f`  
		Last Modified: Thu, 17 Oct 2024 08:15:50 GMT  
		Size: 7.2 MB (7161774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0003de83cdb8d2ad0e8680f26595217fdf942e8bdd548a25a805bb72f3c7d25`  
		Last Modified: Thu, 17 Oct 2024 08:15:49 GMT  
		Size: 15.6 KB (15583 bytes)  
		MIME: application/vnd.in-toto+json
