## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:d1f84490cfe78c67cb117ca58c6be4763f7998dcbf9d04885102422050b28f82
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

### `clojure:temurin-17-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:cf49c6c5e3718862818b68a4af1c27f394376cbf375b78204abe949adb0f5c86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275279903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d663d414806a38ac92b068da3ff0fbe38b0663f2b12c54599f241ad126a468`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:46:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:41 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:41 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:56 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:56 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:56 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:56 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:56 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e290fd8de99763e1069bacd7bb1fa20260be9e90c71e60d41e67c27e7cb2fad3`  
		Last Modified: Mon, 02 Mar 2026 19:47:20 GMT  
		Size: 145.6 MB (145628703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c440cff087b3eac1f26caf8bde681507196d4834dfe582998d1241b075b382b`  
		Last Modified: Mon, 02 Mar 2026 19:47:18 GMT  
		Size: 81.2 MB (81161380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050e1fe2fcc4c157c4938df476ea1eb67c9fa9ef9bdb5611c07b934ba51f03b`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57ecc375a388de4d37deedade91c385a7f7764f042beae947846cd46a02ba83`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0d30165b4cb47927a5cb14a6aca40fd0f01f454cdf2af3c191e828ecaf86f963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7394080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc80217f0670abe409b1ce53bc6c7931644ba2016834a9731e0a03640848ec5d`

```dockerfile
```

-	Layers:
	-	`sha256:fee33fd6377b2e02752f930b40f7af505fa27b0ab0030357e7e3aeb17731b6fa`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 7.4 MB (7378302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:900ff24d43356325cad8cd224918c4a917267acf3942633ff178f1d10e493f9b`  
		Last Modified: Mon, 02 Mar 2026 19:47:15 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:2a7bd58a57fd0dbd3b1795c9da4f501510984b981fd7f5de1392ce253359977a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.0 MB (273965599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10f159fbba47e549e5f7febdab53940bcd0f6c7e5c4ce8d56a41c631fccb1756`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:46:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:46:24 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:46:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:46:24 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:46:24 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:46:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:46:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:46:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:46:39 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:46:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea52a89e667b4cc23dfa17d8a2a9126151e5aff777e0ab873acf71e24c76d5b`  
		Last Modified: Mon, 02 Mar 2026 19:47:02 GMT  
		Size: 144.4 MB (144436183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe1e3528bfe41c11fb3b319ca3dc28242a0e286f00dcb88ee40e872dc83891eb`  
		Last Modified: Mon, 02 Mar 2026 19:47:01 GMT  
		Size: 81.2 MB (81155163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6743ffc41f39d63fd4b43fd83e1ba3ee8647758ddd32ea6fb7b750c4ef8d8554`  
		Last Modified: Mon, 02 Mar 2026 19:46:58 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a475c563b921fe2ce602241c1ac2fc86cf429bb1172af30e848a4d8b5f8e9d`  
		Last Modified: Mon, 02 Mar 2026 19:46:58 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:888243f733034dc8c5e0eee7b86cf9b2b120ac3ef277099fb3487889a1378866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df0626278551ffa14662da6c3e540cc92778587e2d2090e77a74d06464210b48`

```dockerfile
```

-	Layers:
	-	`sha256:6a6912dfd312e98599473d21a08c3aae3869bb7a4181dc1a2f91d35777c4b0db`  
		Last Modified: Mon, 02 Mar 2026 19:46:59 GMT  
		Size: 7.4 MB (7384065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6fb579dfd0650e5b5e9feee891cbf725aace010ca9ae1d836c0a8293f9baf5`  
		Last Modified: Mon, 02 Mar 2026 19:46:58 GMT  
		Size: 15.9 KB (15896 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:528551082a4f81ac80a5ca711a4520a9e0bf7798892ccfe3787c7c9b5063216a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284779979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1f27bccc187d6b5db6c240a1cc72577550384944ef15a491cc700e798735d1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:55:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:55:42 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:55:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:55:42 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:55:43 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:56:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:56:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:56:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:56:48 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:56:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95895bfe1f7b64651ace17069c40ef17497f64e15f57528d1fac95f3e846bd8b`  
		Last Modified: Mon, 02 Mar 2026 19:57:35 GMT  
		Size: 145.4 MB (145438252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c43f87103636e68edbad6bf22efa5dfe441a4c87805d1daa3b3522944e2d2c8`  
		Last Modified: Mon, 02 Mar 2026 19:57:33 GMT  
		Size: 87.0 MB (87003885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4292a195f1d9bdc1d4f961f02e134ad0bf081a3fb1c1ae0e477e7c510777d68a`  
		Last Modified: Mon, 02 Mar 2026 19:57:29 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d485e62ebaee5be5ec1313e24f1d4e08e85af4511b319fa019146fce686df2`  
		Last Modified: Mon, 02 Mar 2026 19:57:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:074904bbb5b72e3c80f4d3a1988dbcba2649446e5b8a1c7151193ca7315d393c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7399344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1589353a6c995b88646c50918ca9f52c8466be626b95ae35a63e53be0f37c`

```dockerfile
```

-	Layers:
	-	`sha256:8dc01227f33333046b234973c6d54bafcbd009be9d6f410c057c1e43a2f3c9a9`  
		Last Modified: Mon, 02 Mar 2026 19:57:30 GMT  
		Size: 7.4 MB (7383518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3e01f699fe8053d251ebc7dfc7a562618235bf72384bc5d108c1b1cd9ec8a01`  
		Last Modified: Mon, 02 Mar 2026 19:57:29 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:555b70c92000029dc5df7c96f3e19f15dcd43cf89e3bb96f59c07ae7bad0240b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262750846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b20e51e03fa70226127354aba71aa51f9ee82920087960e1e2245c438ab4a888`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 02 Mar 2026 19:45:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 02 Mar 2026 19:45:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 02 Mar 2026 19:45:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 02 Mar 2026 19:45:11 GMT
ENV CLOJURE_VERSION=1.12.4.1607
# Mon, 02 Mar 2026 19:45:11 GMT
WORKDIR /tmp
# Mon, 02 Mar 2026 19:45:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bdd7f655825144cbe9055569bfc78b01c44dc2b7156802c817608db9229c8ab5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 02 Mar 2026 19:45:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 02 Mar 2026 19:45:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 02 Mar 2026 19:45:26 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 02 Mar 2026 19:45:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d742a2327b14f9987ddc26394db6a3d975b47be82612e986c876fbe3ecfa10b`  
		Last Modified: Mon, 02 Mar 2026 19:45:59 GMT  
		Size: 135.6 MB (135627087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df21bf61f313548b64fc26ac7f882f38e64303b77ace3402cbdfefaf93e21f2`  
		Last Modified: Mon, 02 Mar 2026 19:45:57 GMT  
		Size: 80.0 MB (79974629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f090c77abad1817af426c9a0dfe14629f7c94889231bdd446b89803497d0772`  
		Last Modified: Mon, 02 Mar 2026 19:45:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb14d70b67f8e1d53e198bb2d6b8e500ed2aa61197bd9fb795ce8ca8a34a01c0`  
		Last Modified: Mon, 02 Mar 2026 19:45:55 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8ab33105be5871782574bde9b0289f971e467fdabda7093a3bb1056c0ea7e15c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7385399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be545e1265fb7401e2a20be0d63705cc640063e0dbb3d7ab563b9a371310082a`

```dockerfile
```

-	Layers:
	-	`sha256:70e80f4b575e06e4d9221ce4c3b5afa11e08321f264427b57a5c3aceef30f586`  
		Last Modified: Mon, 02 Mar 2026 19:45:56 GMT  
		Size: 7.4 MB (7369621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6c4e86f540b18e8f7fcc738da524880c2ce54f656c70ac56b5e4eb9dfb91c36`  
		Last Modified: Mon, 02 Mar 2026 19:45:55 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
