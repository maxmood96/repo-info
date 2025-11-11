## `clojure:temurin-21-tools-deps-trixie`

```console
$ docker pull clojure@sha256:bd535529f25a425baad1de5abd210f5906613ceee97eb672d73ec5341655c34e
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

### `clojure:temurin-21-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:1045b2380593cc0a95284071d9b87071744008e6a4e57b2c2fbff50037c1cd21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.7 MB (292653104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0010b7b7951b3c06cc5cbf8076ea4d059907b7031124785c9c4f022d5dc04df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:44:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:56 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:56 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:45:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:45:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:45:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:45:12 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:45:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2833ede422c52f57fcc0a0c33e3ba000bf4ca4db4a715435942f91fc3819b3`  
		Last Modified: Sat, 08 Nov 2025 23:04:16 GMT  
		Size: 157.8 MB (157825975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc395cc6aff407729103629bb3a077bc8f78fa25b6cff3c1a16c80686f460f2`  
		Last Modified: Sat, 08 Nov 2025 18:46:17 GMT  
		Size: 85.5 MB (85540457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c8691ec5d552403846ec22b7c7eb2ab2e771112b50d5523ac19449912025b6`  
		Last Modified: Sat, 08 Nov 2025 18:46:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7c88a2440f08df70ede55d463b5b2114182094da84fed2920aeb40385d0b05`  
		Last Modified: Sat, 08 Nov 2025 18:46:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:efc021e3ad195692f0fb081f67143f238630d6512784b48b107d8943fc0f61c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7485757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4c81336c2a89c8278ed9708c4217f89e312ef4e427a89c5eacf83b2f84db12f`

```dockerfile
```

-	Layers:
	-	`sha256:f6f57f8ebaf2e30bb1e226b221f60e0c2d6c8984515d546eeed4207327e45b16`  
		Last Modified: Sat, 08 Nov 2025 22:49:55 GMT  
		Size: 7.5 MB (7470003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb924664dbb8673c348bd31878cf2fb964dc40f297454e219ed996ccf03e5242`  
		Last Modified: Sat, 08 Nov 2025 22:49:56 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7f637b464d1ae9a6fba4b3a4206ba3fa3e4a79909fff11cc606664506dbdc537
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291122304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65d4bcf40100e6d63c18411320f78a9b2435f1eb8336c55753731c9be1b7a01`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 18:44:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 18:44:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 18:44:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 18:44:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 18:44:34 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 18:44:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 18:44:53 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 18:44:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e241740d1fd40f58ea45b74df91012845558b913e299f7b5657e7c957ead6b`  
		Last Modified: Mon, 10 Nov 2025 03:50:30 GMT  
		Size: 156.1 MB (156107651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fd31d1670121dbcbddd9439f1f3cd52bc9b9a66aa86542f3dbf1a278d7268e`  
		Last Modified: Sat, 08 Nov 2025 18:45:46 GMT  
		Size: 85.4 MB (85363179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1346b3934ae9e0c1db6688a1a44d1554255332fb58ee038353bef9d672201078`  
		Last Modified: Sat, 08 Nov 2025 18:45:29 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad53ee4593b4b86583ead605ee01454bcafe15a89d169ff5601ddddd86ba39df`  
		Last Modified: Sat, 08 Nov 2025 18:45:29 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:8947ffb2ddc8d0ff455bde30f7bbb8e4189944b6882eb81c6945640d58da7bed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7492905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55d681b12797a5bff7e74efdb8cf01cb5a7bc1fa4e18bfe61ad9f2df3fb60b57`

```dockerfile
```

-	Layers:
	-	`sha256:2e9668fad390700a858029fc004cabb4d9773e0d047c24b863736b3cdfb6c31e`  
		Last Modified: Sat, 08 Nov 2025 22:50:02 GMT  
		Size: 7.5 MB (7477033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f158c0dee4eec81e194f7cfcec66f5685e7e89642b16e20ed4367ceee5d47311`  
		Last Modified: Sat, 08 Nov 2025 22:50:03 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:363c852a104c20e79954973255d92f14730b230ab603a08cff2c0df671dccfca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.0 MB (302003257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c88a7aa2af255a98f508f8f98db4e3a64a2693426bc7e070ad40ae06899164`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 21:34:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 21:34:48 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 21:34:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 21:34:48 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 21:34:48 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 21:43:50 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 21:43:50 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 21:43:50 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 21:43:50 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 21:43:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f62b25a3d3796aee9675283f38cc81cb5638600359ad12a143ed501f80cadd`  
		Last Modified: Sat, 08 Nov 2025 21:36:11 GMT  
		Size: 157.9 MB (157942894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5a608571e974e5b21739ced2e2e6573ce5b917765b27c1f5c141ef3363f511`  
		Last Modified: Sat, 08 Nov 2025 21:44:33 GMT  
		Size: 90.9 MB (90949192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da11478c3388618a4a2865b2a3d9d74ea572e17b2eb4ae83ce49d0b76c59fce6`  
		Last Modified: Sat, 08 Nov 2025 21:44:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb30f508835d90794144ee9b8b6c6549a42a6fdda81f98534e5182e9762c1d3f`  
		Last Modified: Sat, 08 Nov 2025 21:44:37 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:88508105cbe5f79cb8a14c903c84a66df89bc9abbf8df417c205fd8031103c6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e49ca1b6888f249516ef3593a960e2b04caba415f8e4ea0e6de95d1bb7b24d84`

```dockerfile
```

-	Layers:
	-	`sha256:4201e5112f8f91a75564a8f576d39df4f1c4270c198b0f364c54753525eec14d`  
		Last Modified: Sat, 08 Nov 2025 22:50:10 GMT  
		Size: 7.5 MB (7474422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87272147f6eb186e06d99a0f81cd1f72c4a7f5324217f75046a2bd75d26a82e4`  
		Last Modified: Sat, 08 Nov 2025 22:50:10 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; riscv64

```console
$ docker pull clojure@sha256:3f3c827d11a598792a903ce6ddd3d0c6bc2cf8fa9f34bf9513dfcd18c647a472
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289392829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e909a053a98e79f7e81dd7d8348c081436d3f8395301155ff54f996aecf0bba9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Mon, 10 Nov 2025 03:52:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 10 Nov 2025 03:52:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 10 Nov 2025 03:52:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 10 Nov 2025 03:52:50 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Mon, 10 Nov 2025 03:52:51 GMT
WORKDIR /tmp
# Mon, 10 Nov 2025 04:15:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 10 Nov 2025 04:15:27 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 10 Nov 2025 04:15:27 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 10 Nov 2025 04:15:27 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 10 Nov 2025 04:15:27 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:de6b66e2abcf55248485e438d6def9b92cf28773b7cd7896ee78f9409b6e7526`  
		Last Modified: Tue, 04 Nov 2025 00:27:48 GMT  
		Size: 47.8 MB (47770924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5be84f75f5cfb38b82da427fff2f97f31bf8aabe180cf4ebe04e740d623ca5d`  
		Last Modified: Mon, 10 Nov 2025 23:12:45 GMT  
		Size: 157.2 MB (157194308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8eec011c3b8759ec22995899302c15507233f7757c20bcf1bebba1e61eb4163`  
		Last Modified: Mon, 10 Nov 2025 04:20:09 GMT  
		Size: 84.4 MB (84426553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b0492d65e15b12af28821f9217592654cff7714eaa6738f169c154c7929292`  
		Last Modified: Mon, 10 Nov 2025 04:20:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d15995cf148cc1596857c774e0d9e68faf1eddc91d9b6f03aa087bdd6e2340e8`  
		Last Modified: Mon, 10 Nov 2025 04:20:03 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:eabdda8c99e38d70b708f15c90df6fa1c80ada9e4d054c22c87f0c032ca90c9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7473718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b50eca349c45e82bf9da5a10f1852163938e372a612ec00f09de75270a58f5c`

```dockerfile
```

-	Layers:
	-	`sha256:9c44329370a29c86084849dc09d5707f7ac57b41698ace625cf57943fc11a40d`  
		Last Modified: Mon, 10 Nov 2025 07:36:45 GMT  
		Size: 7.5 MB (7457916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e8a3802a22d9f5fdae2c94330619569c002a253dee7d03a507f3bb67ee5e96`  
		Last Modified: Mon, 10 Nov 2025 07:36:46 GMT  
		Size: 15.8 KB (15802 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-trixie` - linux; s390x

```console
$ docker pull clojure@sha256:feb13ab4f6ba0c687c135c2ba3695d282ed2bd48e792d545c69f2986e4ee8757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.9 MB (282931601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d07aa600778997e46e89ac7e276d5bb82fd3f24212cbb4ecf816de8cd3d3e30`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Sat, 08 Nov 2025 20:30:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 08 Nov 2025 20:30:17 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 08 Nov 2025 20:30:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 08 Nov 2025 20:30:17 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Sat, 08 Nov 2025 20:30:17 GMT
WORKDIR /tmp
# Sat, 08 Nov 2025 20:35:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 08 Nov 2025 20:35:24 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 08 Nov 2025 20:35:24 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 08 Nov 2025 20:35:24 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 08 Nov 2025 20:35:24 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a03b440ad1ae9ec56d21ad6945930007c4f3b5f2f34fef5c2ff1ff4580753129`  
		Last Modified: Sat, 08 Nov 2025 20:30:59 GMT  
		Size: 147.1 MB (147069867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f009c20b313004d6e088d37c963eb08266db1ab670c958f47e7c32d95f75c6e5`  
		Last Modified: Sat, 08 Nov 2025 20:36:08 GMT  
		Size: 86.5 MB (86508391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26952c23e178c553e6eb9ad8e744d9546236b332b4cb206fffdaa972f8fa37b0`  
		Last Modified: Sat, 08 Nov 2025 20:35:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:494864bb8d8db96da5881ab78b0acb7ad295dac1ed000bda748dfa2ceb705564`  
		Last Modified: Sat, 08 Nov 2025 20:35:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:134de834a64e2f7ba29f6cf31d4ab4dde8b16f69f313aad68c92ac804455b645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7481679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a8b19a3d2c5a5c21febd7652ca6843b2b72e83a7e9f2911d14b6ce11153ff8`

```dockerfile
```

-	Layers:
	-	`sha256:7514cbfe07b0c9b06f44e8d6d7783498faa583d8761e17fee10957cff871aa45`  
		Last Modified: Sat, 08 Nov 2025 22:50:26 GMT  
		Size: 7.5 MB (7465925 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d20327cb2daa05a135f551179964eee016f4b38ac884a2f66152646c66ed241`  
		Last Modified: Sat, 08 Nov 2025 22:50:27 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json
