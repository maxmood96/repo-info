## `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim`

```console
$ docker pull clojure@sha256:bdbbc7525b6302ccfe5596e928720499b55c831b4c4910e6b6f73f2f57849b20
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

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:83f1ea850304f147d050fbcfa20330ca5d50fa643d2360c02c5fbf18d2320abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194402988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e957f9fc534fca1813d73e63cc06d7432000f7c6a3f71d0d8ebccf00efeaec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:01:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:41 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:41 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:01:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc85245d4e02b9fd58e5ed970d17d53f661c90e04bca983607fb9378943415f`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873cddf6b50f71ccbd8b31cffcd827444a62a73025a2f259aace424c1d74ac0f`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 72.0 MB (72047456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebaa6112a7513f22d111c3352827c4db6d3e674603ad8bc757c8a1608c16923`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d93b069544f3941cb2aa4ccdd14c62ce01eda1a971310d324d10533963cf8`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a9a1d4af59fe677f23e79d22bf6a077f5c014a582be8472e38fcc720fcd487b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ac2f40498278258601deef4ff1513b66105ab021f108aba8a1fa51492e9c22`

```dockerfile
```

-	Layers:
	-	`sha256:c98c55e1a4ad9eaf53b81ae3f0e24753182a85735b1839eb2f4cb9d3b693f853`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 5.2 MB (5228049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b42d6e652067663fc073301a71c9b15f30ac6e0008d73874b202b3186cdf160`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2ac7f9a68877a061fb1da01e30a92405940ca6cd922b3327d42789fe055a2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193557458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddffe33dbeb40aef7eeed053492860297b6c0c8d931c64b81b41bf77b0037d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:28:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:28:37 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:14 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02a0b02b0a2fee546440b8b26e911492900960a48ada515d3f3d1f5ad32022`  
		Last Modified: Tue, 19 May 2026 23:29:25 GMT  
		Size: 91.5 MB (91542270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632cebfd99c98fb4701c1b9369c61668712375ed97c554a1c71ec25038309eee`  
		Last Modified: Wed, 20 May 2026 00:08:49 GMT  
		Size: 71.9 MB (71872231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a0682bcf72e5946834dc2f3f8fc18899e19b289bf115dcbfd51abf5c6e2a49`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ebc6c883c2855de75563e86aad57d0a13fa99cf43a14abcfc236c1de717f25`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a2795e33a185a3eddda0f9ff45c6cbf170a0257e9e166c9711159709d889c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612029fb610fef27398ee45995145a971448b0bc65ff461b47cbaf5c35018284`

```dockerfile
```

-	Layers:
	-	`sha256:0e1ccbd4270baa5b89a931cb64e0b706090aefe93ee2cb8aeccc07f3164dedbc`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 5.2 MB (5233831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e275306d74781b91aa6db6d45827be0b9d4aebab3b6236a133b85339e5449ae2`  
		Last Modified: Wed, 20 May 2026 00:08:46 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:1d6a9b2484891be180de0347238c58165a36df8dd4f9656f851b7bf96e151c7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202981529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a5bbb78bf24fb9134054bce1384d7d48c4d86827681e6616acd9e052796384`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 06:06:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 06:06:59 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 06:06:59 GMT
WORKDIR /tmp
# Wed, 20 May 2026 06:10:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 06:10:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 06:10:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 06:10:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 06:10:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe901bdfd8966081270b7ee3a299c954c200a642ef0bde8cc9488b26992dfc68`  
		Last Modified: Wed, 20 May 2026 06:08:03 GMT  
		Size: 91.9 MB (91914021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e7dad167e3a46e45b107c1f1c5b338e2b3f27a0eacb5ae52d190c177039cc8`  
		Last Modified: Wed, 20 May 2026 06:10:45 GMT  
		Size: 77.5 MB (77466013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0642f4c2a5f9d98b564caa016ac25e11ce100797fcc039df7965118da78382de`  
		Last Modified: Wed, 20 May 2026 06:10:42 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9d89d75e720434394c8c7097740f5b594f9c38eee24d6ea808ed1e63d28e587`  
		Last Modified: Wed, 20 May 2026 06:10:42 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:24be9d4c7777c2560ee5da5aa0e51f3d73657daf04a8123fd9448cabcbda3c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13e5cb49264a7f51748713c923e6134d465f3ff0486ee43aa668cf7276f6bd0d`

```dockerfile
```

-	Layers:
	-	`sha256:397cc31dbb0510f7571a950d43c91a7e2c41a553809364a009226415e4e08dea`  
		Last Modified: Wed, 20 May 2026 06:10:43 GMT  
		Size: 5.2 MB (5215744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e776853d172b27133d63c0d0a9b3d207a61c01677ec3e49a7ab2e0593df47195`  
		Last Modified: Wed, 20 May 2026 06:10:42 GMT  
		Size: 16.7 KB (16707 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:1831a883f2ff7d188f69e38e2af0cc7bca63e22c2429cfe079f5dcaf4d3d02d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191297118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2679ae168403f1e92094317377065944f0fdd324b84848dd6fbd6397956c9d4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:47:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 01:47:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 01:47:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:47:28 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 01:47:28 GMT
WORKDIR /tmp
# Wed, 20 May 2026 01:48:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 01:48:41 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 01:48:41 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 01:48:41 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 01:48:41 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe63f38fd6a445c3c5a37affce45515ef2df366f1a8ba589effaaec1088932e`  
		Last Modified: Wed, 20 May 2026 01:48:08 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee726397424cc076727d790cf0c19e2de2f4f6e34df1583466dd384d66be1b79`  
		Last Modified: Wed, 20 May 2026 01:49:06 GMT  
		Size: 73.0 MB (73029836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56e64edfa8f2b44c1f2f5262551c9e55020637b86e552de5ea5e67a1eb2202e`  
		Last Modified: Wed, 20 May 2026 01:49:04 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70477313c576a51be781ee643fea3c1f92bb73692a5e0baa150f271c959e8e8b`  
		Last Modified: Wed, 20 May 2026 01:49:04 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1645-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58d5f53909452ec56da9400ddf5d27a865f4303a69dcf20a76501d1a1fed2b9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441487164203f230162d19237b1ef967d6dc69f5657f56629d43176e9860131e`

```dockerfile
```

-	Layers:
	-	`sha256:01bcc1f64074cf268070daa3286d3a1525b4de11b5c7b58972998afb8881bd2d`  
		Last Modified: Wed, 20 May 2026 01:49:04 GMT  
		Size: 5.2 MB (5208535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b4507614684cffac4b24364c6c6fa965dec9b7821b5628f4fbc3b4dc03db024`  
		Last Modified: Wed, 20 May 2026 01:49:04 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json
