## `clojure:temurin-17-trixie-slim`

```console
$ docker pull clojure@sha256:8a45ba240c87743b8cd4e0e2a8a289306bfaf8aa12286fb0f8026ba11d6b7834
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-17-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:98defee192276da80c9b63cb284191dfb7bda463156438691f1c623a38e83d42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.6 MB (246617990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c8b31ed8605ef0656ff936a22f782d9d5b7d427eb660741b498dc59d15d95de`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:00:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:00:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:00:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:00:50 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:00:50 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:01:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:01:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:01:05 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:01:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:01:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6ec4a1f81fb9d4bb0bdcf49451f2a89136f8e47895884ca35a7eab24cc71df`  
		Last Modified: Tue, 30 Dec 2025 01:15:30 GMT  
		Size: 144.8 MB (144847921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c91cc1016c9331249de5760f78728527f7273b29dd47afa3564570b7e3c6d3ce`  
		Last Modified: Tue, 30 Dec 2025 01:01:41 GMT  
		Size: 72.0 MB (71992498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0105f02e5a3191e68afb08b5151fcad2abbc9c27aeb31ca857d7c3470bc6bc`  
		Last Modified: Tue, 30 Dec 2025 01:01:31 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9763680a3e7b176ba47e83ce5f16ca19927301b5bc55d865fc252df05f7c50`  
		Last Modified: Tue, 30 Dec 2025 01:01:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:77bcb6f3f7e1b11cbfd2e6fabd0ac4d1292b7cf2dd628c17ef8244d4662540dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5272011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cde9aa0375883a400c91ad1714081a8cb02b19f2d789e22af721bce44df7b1c4`

```dockerfile
```

-	Layers:
	-	`sha256:22839feb2dfa8087abce5bb1bffb377911828a0aafe53565af61041c0cc683e9`  
		Last Modified: Tue, 30 Dec 2025 04:42:04 GMT  
		Size: 5.3 MB (5256199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efdb3fc56d4d8622bfcf3173f07779c4df647a9526ec3499a3191f827e22da4c`  
		Last Modified: Tue, 30 Dec 2025 04:42:05 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b1325ccc4ead635eb33d68d3ba9a676469454dabc3375e4f561a7143037099a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.6 MB (245626245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a509bc4ade6bc9db048a3710d209456318ebd06ac07681482dbd6c658655309`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 01:01:49 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 01:01:49 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 01:01:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 01:01:49 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 01:01:49 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 01:02:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 01:02:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 01:02:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 01:02:07 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 01:02:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab98cc6d1595fee341ae9fc25b3b594249ff35c41a6d2c2a384f6eb2edfd9414`  
		Last Modified: Tue, 30 Dec 2025 01:02:55 GMT  
		Size: 143.7 MB (143679920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6edda0f47fcae7239c858fe9147ac9be10159947d0de7f8f34e99da310e0f607`  
		Last Modified: Tue, 30 Dec 2025 01:02:52 GMT  
		Size: 71.8 MB (71806648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c32ee8ed9e0ddd78b15d6a3e3425405ec33d440f7f0167c200dee974c0c2ba4`  
		Last Modified: Tue, 30 Dec 2025 01:02:37 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd80b0000d501b48da7134381289db2d3a529e220a1b845da96f25acb7f394b`  
		Last Modified: Tue, 30 Dec 2025 01:02:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ec112a99c4b603fd224d6ac98f825410849fcef533e37992ba28d797922188dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5277898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b91aa002c8af4b1c88c14d27c88f5bfdcad742b26ad2aca1923ac6e621e02e87`

```dockerfile
```

-	Layers:
	-	`sha256:68e0d2c819d50ffcca46720469dfb2a61869f40eb38b0efdeba2b265e1276c84`  
		Last Modified: Tue, 30 Dec 2025 04:42:09 GMT  
		Size: 5.3 MB (5261968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83044a7a87f3c45ceaec13cd60ec0a9558fe2535101bf8d123fe359f2b2ff9f3`  
		Last Modified: Tue, 30 Dec 2025 04:42:10 GMT  
		Size: 15.9 KB (15930 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:5d2c2711b2672e3410343f1b2b515b8a93bb8236c8e3c6f6407a4bf3b6b3f00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 MB (255510143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc737b5715182d0b32e666b2efa023bb44d6b3c25a164ff98ad5cbef467d4162`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 19:10:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 19:10:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 19:10:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 19:10:02 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 19:10:03 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 19:10:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 19:10:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 19:10:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 19:10:47 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 19:10:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6e459b5cb1f7cbeb835d5f2c62bfb93c7f279db102bb5edccff8d14681becf`  
		Last Modified: Tue, 30 Dec 2025 19:11:58 GMT  
		Size: 144.5 MB (144525219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:281a85467c57493e7458deef9b04f84bb7a4ba55dfd44b6a67c8ae8f2787074a`  
		Last Modified: Tue, 30 Dec 2025 19:11:52 GMT  
		Size: 77.4 MB (77386989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d03c5284eda84538d5a32908bcc3b512a7afc92712c1db83f6ae36113a6494`  
		Last Modified: Tue, 30 Dec 2025 19:11:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7f4f5a452adf24fc525ad521db31e55139535606c9f9374261b1c520f81ed3`  
		Last Modified: Tue, 30 Dec 2025 19:11:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:36b0acdbd1e793f019d551cd894f3139f4039df897995cc3439fc46f1237a22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5276429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90a214a78219b5c6067962c1b919d7373eda320f03c5672dc1b1bc99b5a5c0a`

```dockerfile
```

-	Layers:
	-	`sha256:e4b7aaaacd3263e94d7e3982a172f6f0e8c812f3a77873097ce7496799dbdb2d`  
		Last Modified: Tue, 30 Dec 2025 22:36:04 GMT  
		Size: 5.3 MB (5260570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91798e3337432accb890c69b4d46385264e8741b6049818ed147201ff19638b3`  
		Last Modified: Tue, 30 Dec 2025 22:36:05 GMT  
		Size: 15.9 KB (15859 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; riscv64

```console
$ docker pull clojure@sha256:dab5c1b25506b2b223e1f68d41c84476f98742f067e4c90bd73ea4f5c3684553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.0 MB (241041888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6108397a705ab2300207842728e2dad09e68b3253891debbf0879d7a3f47ba4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Sat, 13 Dec 2025 18:46:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 13 Dec 2025 18:46:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 13 Dec 2025 18:46:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Dec 2025 18:46:20 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Sat, 13 Dec 2025 18:46:20 GMT
WORKDIR /tmp
# Sun, 14 Dec 2025 16:08:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sun, 14 Dec 2025 16:08:28 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sun, 14 Dec 2025 16:08:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sun, 14 Dec 2025 16:08:29 GMT
ENTRYPOINT ["entrypoint"]
# Sun, 14 Dec 2025 16:08:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d48c227efd13f09a34b153f418d7d540a21d31aecdd5fd15ad6529d2a559ad99`  
		Last Modified: Sat, 13 Dec 2025 18:52:43 GMT  
		Size: 141.9 MB (141889553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78efe06b7cfaf4c0a1d7b9cae49a177e3d280a75aaa44ac3c8b5fd7d5010d31`  
		Last Modified: Sun, 14 Dec 2025 16:12:22 GMT  
		Size: 70.9 MB (70878139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c104a843b30739f7bfee3c61a26fff06c88fd670d41404c04df29fa3c324cb7`  
		Last Modified: Sun, 14 Dec 2025 16:12:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e90fd04a522bed8828fd409c258f0e239327a5178d734162b6d533cd8dd61989`  
		Last Modified: Sun, 14 Dec 2025 16:12:16 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:199778d736a9b8c008baef05bea93d6cc220f74e6dc39d74cd2636a95bee020b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5259604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079852dd14e8bd31b88c1fbdb5cb07f9daadd0f8defb211e49e675dc1b0dcb6d`

```dockerfile
```

-	Layers:
	-	`sha256:4e5463f6e7dae0c70304f85de141dd7a87b8f3f68a7f4b98a83af8a4ea00dc72`  
		Last Modified: Sun, 14 Dec 2025 19:35:40 GMT  
		Size: 5.2 MB (5243744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d3b7c246e159c516b3d04a32a3ac0fe44bb9992d493b9ac1316f3471b66e8d0`  
		Last Modified: Sun, 14 Dec 2025 19:35:41 GMT  
		Size: 15.9 KB (15860 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:57acc3717475ac829e2348dc3938bed69d60cad12da40b08697dd95c517db008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.6 MB (237647789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fc4d268e303f19767df4cbdde1a4d43dd4ba99c49be2bc41bc53daddd21dd7b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 02:03:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 30 Dec 2025 02:03:47 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 30 Dec 2025 02:03:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 30 Dec 2025 02:03:47 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 30 Dec 2025 02:03:47 GMT
WORKDIR /tmp
# Tue, 30 Dec 2025 02:04:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 30 Dec 2025 02:04:03 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 30 Dec 2025 02:04:03 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 30 Dec 2025 02:04:03 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 30 Dec 2025 02:04:03 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455e9f9f60ff6c76abf17e11a97212c5b4c569290bfc0d73f8147ac5ca5bba53`  
		Last Modified: Tue, 30 Dec 2025 02:04:47 GMT  
		Size: 134.9 MB (134859063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8c8050c53a5f6c65945aee2d88875b1b533e3b274aec662721fa852506609ff`  
		Last Modified: Tue, 30 Dec 2025 02:04:45 GMT  
		Size: 73.0 MB (72953269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e9779819699c4839982b7523dd57b57bf315240e87394ee0868b5750ea63d7`  
		Last Modified: Tue, 30 Dec 2025 02:04:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:583af7cb1ddce38bde43243afa466e38d0d20daee2ab5162b8ee3e7a2feac7d5`  
		Last Modified: Tue, 30 Dec 2025 02:04:38 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:42fb66bda0936edddb483eba4172717ccfbb7eb4939bd5e059e76a8bff70f7d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5267935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c299c8b831433b67c6576aac43d4ac21f9da751364c8a01eb7cf035c22ad3e`

```dockerfile
```

-	Layers:
	-	`sha256:122f1d281a3f953ff3740c22e571f07f03ca7f95c85fe1b65659df2abbe8f4e8`  
		Last Modified: Tue, 30 Dec 2025 04:42:22 GMT  
		Size: 5.3 MB (5252123 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca9a74a1a0710698e51c8deed290c9603c4659b5781f49b90796317b510ec05`  
		Last Modified: Tue, 30 Dec 2025 04:42:23 GMT  
		Size: 15.8 KB (15812 bytes)  
		MIME: application/vnd.in-toto+json
