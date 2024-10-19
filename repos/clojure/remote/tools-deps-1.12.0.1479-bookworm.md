## `clojure:tools-deps-1.12.0.1479-bookworm`

```console
$ docker pull clojure@sha256:f037d21d374a8731aff77b88f0c41bdbfd9a71e63da2c9c4182b10e400e2394a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:0041d1a83e8d833eabbd194f16dcee40717d529631c57c954e228da054ac1f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.1 MB (289063396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28c0aa9198a24d44bc70997ebec1c7f806bd000b9cf6b6c582991589b2171193`
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
	-	`sha256:ba65de38025fcdc65bb50a396caf55cba7c87535bf8d81b0cf4cf5091ab45889`  
		Last Modified: Sat, 19 Oct 2024 02:59:51 GMT  
		Size: 158.6 MB (158579322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1282fbe52681e7f8628e6eff3cbfc88edb1ef909ed8e472668ecf58ae80dd74`  
		Last Modified: Sat, 19 Oct 2024 02:59:56 GMT  
		Size: 80.9 MB (80928011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2ac2b5803dcc8453e7823e654f698d2471c707d89bcd10e989b18b6ce14a2c`  
		Last Modified: Sat, 19 Oct 2024 02:59:54 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e7c464b3d54ed4e29045a3d9e095a332fb3c32e3cbf3eada548c326b5d23b8`  
		Last Modified: Sat, 19 Oct 2024 02:59:54 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:da27c2a75b7afa467fce5b82756b3ea619da10a912c98f0b6284bf5bcff8ae17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7205138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a6bb244443077727b2c76ad08a1a3bd6f2a601037deca52b6da53ab64b34a1`

```dockerfile
```

-	Layers:
	-	`sha256:e1edf86d67733b15bc478020c765207df57cd675a973a371395c3dec137fa243`  
		Last Modified: Sat, 19 Oct 2024 02:59:55 GMT  
		Size: 7.2 MB (7187492 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92ba13233c5ddd859e0ccf57ebcf68f912d4583f03ce5855cec9ae157bb4852f`  
		Last Modified: Sat, 19 Oct 2024 02:59:54 GMT  
		Size: 17.6 KB (17646 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1e27816a80cee76298bb9a20404a6e84c704845fd425fdb32e28159190ea8c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.1 MB (287122266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3e7ac5011b906f19dffb482cd5e6d9c34598d54142c955cc0b42556aa9ec13e`
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
	-	`sha256:6081bef755cabe28916d335d34f5e5bff03f6905db8f85e9e22d2927f98411a9`  
		Last Modified: Thu, 17 Oct 2024 07:54:30 GMT  
		Size: 156.7 MB (156746192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e21c332a61721f87a6ce622518a613e108366928b4035a527c56b208c9deb74`  
		Last Modified: Thu, 17 Oct 2024 08:23:01 GMT  
		Size: 80.8 MB (80790054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c23d5f751a68fb74937aa3119c1af668be06b9617c105674a47cd29ca20e2a0f`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a7b4c59a9ff684bc17cd35bc69a34b1a24a94cb1b5876caaa02816677dd2446`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c3013576dde8bb5b2dbf531e1007965628a2512cce641532cc7458b8c9dc0299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7185243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedd10b9bd72ba2dbe804298112f5790ce90c62764084a7fefea1b39ea41e5c1`

```dockerfile
```

-	Layers:
	-	`sha256:3dab7c8d34dbd5f1ebad5ad50e1645901ddf0246fb03423ce09ef08e8a011ba1`  
		Last Modified: Thu, 17 Oct 2024 08:22:59 GMT  
		Size: 7.2 MB (7167587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcfdbc6c65b750289a607a77b84e0d6602d949ef9587feda44b7f292e93b71b1`  
		Last Modified: Thu, 17 Oct 2024 08:22:58 GMT  
		Size: 17.7 KB (17656 bytes)  
		MIME: application/vnd.in-toto+json
