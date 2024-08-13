## `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm`

```console
$ docker pull clojure@sha256:012de34d683c2826f78056c33196c82ee6bcc4f9305c1e0a7452399a4c6bafa5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8b8e2404f55113dc2dfdc70f4e12cc410eb4cfca5a1e149cdd0b3b254e806fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286490276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fd89f3134bcfd47f546256927c6c6c5932ae239f99133209d70d67d074842e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:0d5bdf84bbcdfa95d42190537e3cad2c0a5876f9127fae6a1d1c485d3539c77d in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:903681d87777d28dc56866a07a2774c3fd5bf65fd734b24c9d0ecd9a13c9f636`  
		Last Modified: Tue, 13 Aug 2024 00:23:26 GMT  
		Size: 49.6 MB (49554080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa80d10354fa56b380ae225a693e38a2e035b914320914975b9ecaf5bde3281`  
		Last Modified: Tue, 13 Aug 2024 01:11:47 GMT  
		Size: 156.5 MB (156481595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b132b9304d969881b9674f2c7eb05e47d74433b1d811fabced4f8dffc8eb3ac`  
		Last Modified: Tue, 13 Aug 2024 01:11:45 GMT  
		Size: 80.5 MB (80453563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5fdbd218f3c0abcabe90dc4242190ac49b5d7d12d23065f8594f9c9194df06f`  
		Last Modified: Tue, 13 Aug 2024 01:11:42 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32b3e0236330484b9363599c79637a047f2d17094ba0c4e77bb5b0c8706c311`  
		Last Modified: Tue, 13 Aug 2024 01:11:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c1501f7f369843643e8d595619e4850a5f7c12d7b98180b6a0fd9aeb306f2b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7016888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a1f081239d1a8b14785c13f8d9de3cb6eaef8abaa30090db3adeb6e31a4a335`

```dockerfile
```

-	Layers:
	-	`sha256:d165d2b539a62ae173af8d98c74033339a5d8b9c57c03c0ff35d23cecc95f445`  
		Last Modified: Tue, 13 Aug 2024 01:11:43 GMT  
		Size: 7.0 MB (7000764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:856ca734240d5b82ba3248c7bbd38ea9c200a56d2e50634b6daa0d8006cf59cd`  
		Last Modified: Tue, 13 Aug 2024 01:11:43 GMT  
		Size: 16.1 KB (16124 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:caa599f3abdc75fb147852a54c7223f9aa291daca0eeda55614ab51f4b0bd784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.3 MB (284291672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738b696ecb29465cc9f181b5479219aced7db3e84f31cb988c2cef2fdd92794b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jul 2024 04:17:40 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Tue, 23 Jul 2024 04:17:40 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4c9a1a0bb41bcc3f3a8491c350442160b221aa7c51caa60ace0f14d32c1f18`  
		Last Modified: Thu, 25 Jul 2024 21:27:19 GMT  
		Size: 154.5 MB (154503755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdccece4ad8019632b5d19898ebd04e970ce719c655cf415a323565414a89c7d`  
		Last Modified: Wed, 07 Aug 2024 20:17:00 GMT  
		Size: 80.2 MB (80198433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1452032224d987a2773c916f135bcbe55d6b6cbcc0596e2eb3fe5e7fb875184`  
		Last Modified: Wed, 07 Aug 2024 20:16:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f97679705ab91010d294a6ddd0fee419ea44a14e44c84d76450bacee0aa45`  
		Last Modified: Wed, 07 Aug 2024 20:16:58 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:12753c71f594bce703c532b06010dbc4ef92b61e1e41ea3710a8948b3afb69a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7023859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab8be9c262a1aeb20e16062605be365c4f245b3ac8027abb4ceb5a64cd9c9f3f`

```dockerfile
```

-	Layers:
	-	`sha256:7876a5101e2e958b87cad2113e4ccadd3c729468fb96880e3aa544792129c28d`  
		Last Modified: Wed, 07 Aug 2024 20:16:58 GMT  
		Size: 7.0 MB (7007175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e150e965175a30187c1f6e9c1570bcd186b7fa7771641bfa9a18373e66bb9b3e`  
		Last Modified: Wed, 07 Aug 2024 20:16:57 GMT  
		Size: 16.7 KB (16684 bytes)  
		MIME: application/vnd.in-toto+json
