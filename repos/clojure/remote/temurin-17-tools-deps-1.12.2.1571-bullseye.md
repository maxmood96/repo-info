## `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye`

```console
$ docker pull clojure@sha256:ecf88b43a6ba4f59b3ac277d54d2d89289c7ac75474ce0d212d7dcc4a694265b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a9d1b827ba240a0328eeaf7b3d987e622e5a0c6e17c97d248c542c75215f400c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.0 MB (268010453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ccf387aaa2c40d7dd594073912e536e9dfd859c40cd671a94794f3190474682`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a749e8f08a4695231ffd1acd3d9cb3b0ecf06bd35fab3edacb0fc16986ec4e0`  
		Last Modified: Tue, 23 Sep 2025 01:45:26 GMT  
		Size: 144.7 MB (144693608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562d7dd930cb3c82b05816b6662c357aaa3e99bc424995fe0cfb585429fb29f6`  
		Last Modified: Mon, 22 Sep 2025 23:46:18 GMT  
		Size: 69.6 MB (69560405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a142608104bcd969799984c277ce0bbe0400c8ef6d5ef84bbdc371602185f5f1`  
		Last Modified: Mon, 22 Sep 2025 23:46:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3caa20fd2053e13d16389837f6702ec71efd992d17529374da9104237a26d5`  
		Last Modified: Mon, 22 Sep 2025 23:46:01 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:373e4a7e3b655e74c273056f5d771922aa65d64fcb57343c123904b0a48df88a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7411488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9758a0a042512928389e9d0e0e1cdc151a7b2b82839e984634b16b2a84d3dfaf`

```dockerfile
```

-	Layers:
	-	`sha256:354bd417a53dd5a7e9f6f0b7847dfd28b976c13f5a5a46ea08e31a2ee50f3404`  
		Last Modified: Tue, 23 Sep 2025 00:38:06 GMT  
		Size: 7.4 MB (7395667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3d705ac7d9a5d7543cae307e5e9f8cb72fe962c5fe5f47eab535fae03ee23ac`  
		Last Modified: Tue, 23 Sep 2025 00:38:07 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:06f291bdbb9a42f5de44ee5b19e989624175d5015efc4da24742d4f89078c7a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.5 MB (265479362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a338e22971fd640fbf513f6fbc8317a7f7f46c99178934bf3cb5e9fd282981cc`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1757289600'
# Mon, 22 Sep 2025 21:54:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 22 Sep 2025 21:54:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 22 Sep 2025 21:54:33 GMT
ENV CLOJURE_VERSION=1.12.2.1571
# Mon, 22 Sep 2025 21:54:33 GMT
WORKDIR /tmp
# Mon, 22 Sep 2025 21:54:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "14c532e6e2dd760c7bf9d5fdd2044f4ea63e11c9126b89d4e120591352499fff *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 22 Sep 2025 21:54:33 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 22 Sep 2025 21:54:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7df02cb4a974a4e8a9eb65ffcff7274f9dca341d29aaa763294c42e49805ca19`  
		Last Modified: Mon, 08 Sep 2025 21:15:41 GMT  
		Size: 52.2 MB (52248370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0d855f0718fbe1c88b97d104e22c6e503fdd19a4a6e2bbd848f0cfb40ace4e`  
		Last Modified: Tue, 23 Sep 2025 20:24:13 GMT  
		Size: 143.5 MB (143542122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9355777f0d62aa39a00ca8547990cdc62f0282453a0c0e9748e9efa1079f71`  
		Last Modified: Tue, 23 Sep 2025 20:24:03 GMT  
		Size: 69.7 MB (69687830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5598f23a063373c7dec57d8f2acb5c9b7bd0f28f512f5e88ce5501b4e6e6376`  
		Last Modified: Mon, 22 Sep 2025 23:07:11 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3f33b743062397a7b1f8d11f878920d38ebf609da1f4f7fd1f9b9b033047df`  
		Last Modified: Mon, 22 Sep 2025 23:07:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-1.12.2.1571-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:069ff018172e0d6ddb7df9049f99b98c952bdce9024f21edea836bbe0e9c2dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7416705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63322022f832be7773f8b128b0fdbd64003472704b1fbc5fb777eae115cd3c83`

```dockerfile
```

-	Layers:
	-	`sha256:a29df948014a0addae9008cc2b6f429830c085f6dda393518510cb5828ac2936`  
		Last Modified: Tue, 23 Sep 2025 00:38:14 GMT  
		Size: 7.4 MB (7400766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc9261774426a33985f9b99e4cc52733d1e1fd26feea912a027d6fa0ee81859b`  
		Last Modified: Tue, 23 Sep 2025 00:38:15 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
