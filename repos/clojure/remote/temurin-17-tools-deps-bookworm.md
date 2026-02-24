## `clojure:temurin-17-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:a736eb223c22fc90bf3b69c220fd098ff212b66af926303141a3811df2bb647c
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
$ docker pull clojure@sha256:bba7b0137566e370681abb2dc90a84d70beb76d3062cc8627828fa4c5481f4d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275268835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31ef1bb053238c252646bd0b0a38edca012206739569e234023b5aebd371fae4`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:54:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 19:54:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 19:54:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:54:59 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 19:54:59 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 19:55:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 19:55:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 19:55:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 19:55:14 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 19:55:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde387eb91f78f5d1a862944eeef301640d3c10ec942c4b96ceae697bd9bfef2`  
		Last Modified: Tue, 24 Feb 2026 19:55:35 GMT  
		Size: 145.6 MB (145628702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d174829e61f30147e65039570303ad3eb72a237799c6cc59c761d3e57a1046d8`  
		Last Modified: Tue, 24 Feb 2026 19:55:34 GMT  
		Size: 81.2 MB (81150318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8633bc8d5f6aac34324e8e16f56665db9e611192d6ab01e151ba5fb89162253`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a2aa621e82912ab9e80f6ed0dd640fdf898acbacdc7c3507dca00587cfcde86`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:40de46a1053fa424ddb88e0a59bcbe04d611ef5a09183e850b17f30a2e041fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2356149013124442ac0cdac5e9faf9f4e87454c473d2865b7a7c851b67a8257a`

```dockerfile
```

-	Layers:
	-	`sha256:4183531419d3311230f230912ddc8fba06af457adb480ec9d63ba093a15895f1`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 7.4 MB (7376789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cd892416fe2ecd4fd59eb000437145a6aaaf0be427bf962d78bcde5f7449d9d`  
		Last Modified: Tue, 24 Feb 2026 19:55:31 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:deab60d59376aedc93428ef2a3ecfbcfcda810b630fb940b7b21adf7cfd5ff7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.9 MB (273948765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34fae5f60ea91ec3d051d91be5e18f26882805727a295ac594ab2fdb95222cf9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:05:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 24 Feb 2026 20:05:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 24 Feb 2026 20:05:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:05:44 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 24 Feb 2026 20:05:44 GMT
WORKDIR /tmp
# Tue, 24 Feb 2026 20:05:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 24 Feb 2026 20:05:59 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 24 Feb 2026 20:05:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cbaee4f23c8e61222463cb0c3e7e598081dfcf5feec098a5558f0953658fe8`  
		Last Modified: Tue, 24 Feb 2026 20:06:23 GMT  
		Size: 144.4 MB (144436198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9894895dafec59a065a76c9673fd4a03b83b13e9ce6e50507f3dafc705be709`  
		Last Modified: Tue, 24 Feb 2026 20:06:21 GMT  
		Size: 81.1 MB (81138319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:219ddaf9fd31cd97b8c1c887b53cb93185fa74efcc1bfd1b35cf92680f190522`  
		Last Modified: Tue, 24 Feb 2026 20:06:18 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f0c247655838499b8879464fb147ef038165b7d968cb9397082ff16f8f20e1`  
		Last Modified: Tue, 24 Feb 2026 20:06:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:7e98b3d2927615601c2442766a77e64bf0fa815c40c5fd79b128679d57924a9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0dde80428eda4be8b6ad0134bcf2851c280db7e215b120ed1eed652fd178cc`

```dockerfile
```

-	Layers:
	-	`sha256:505c8a9593de0545166cddd29b182efdd7886d06dcc2d606782f0e3168eb5786`  
		Last Modified: Tue, 24 Feb 2026 20:06:19 GMT  
		Size: 7.4 MB (7382552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4a7574fcf52d8308375827a9f7b8b5f76ffe41e78c15860c92a9aed0eed4072`  
		Last Modified: Tue, 24 Feb 2026 20:06:18 GMT  
		Size: 15.9 KB (15894 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:f012e31ae716a00efdc0f4140d08ce963ae3bc548792140293d357399f368ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284753733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee2d01ef483a466e9fce74ae23c0249e7d225d3374e3b6395a937c57d548cd8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 23:45:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 23:45:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 23:45:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 23:45:07 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 23:45:08 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 23:51:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 23:51:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 23:51:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 23:51:43 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 23:51:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5e189aacb842725e8d1d9877c9ab9af09e14901412b6665e179393112b5bca51`  
		Last Modified: Tue, 03 Feb 2026 01:12:57 GMT  
		Size: 52.3 MB (52327289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d2bcebe1436b2e06a46e1026a9f267beb7b738921e7b714b94ecc1b9526b812`  
		Last Modified: Tue, 17 Feb 2026 23:46:43 GMT  
		Size: 145.4 MB (145438175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2ec25b5b4b77d0be2c0e13d34b98eeca85dea2f994c87a633eda9c91ae2e05`  
		Last Modified: Tue, 17 Feb 2026 23:52:26 GMT  
		Size: 87.0 MB (86987224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40eccf9a120a020ec35bfa7bd8b45f4a102b2229ecfc9ad328742f1905cbc8db`  
		Last Modified: Tue, 17 Feb 2026 23:52:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe3968773ccb607047341bae3f5f302d28880d52bf8df3af77b3a969391d7344`  
		Last Modified: Tue, 17 Feb 2026 23:52:23 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:bab88806d93f88a22d5e59c0aef79dc71eff2b0ebc99968226fd8c650f2eac9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5e02cc67357d086bfd2859b155e862d3be4924787679b1cbed87e6764bff676`

```dockerfile
```

-	Layers:
	-	`sha256:415a15517a3708c3d1538b4295fe034f67914f146fdd86c8cf63303f23f43e50`  
		Last Modified: Tue, 17 Feb 2026 23:52:24 GMT  
		Size: 7.4 MB (7382005 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5355b65ae0cc9dd3a3951fce0e824393d35c5feb10763727d022ed6f7951660d`  
		Last Modified: Tue, 17 Feb 2026 23:52:23 GMT  
		Size: 15.8 KB (15826 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:f0d9d0eba696eeff4e39cd5a140ff37d3b6867c058c2587530f7fd3acdcd6c5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.7 MB (262730139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b5f9427977557b57eb438de56b7962f4b5d2e286b97c6a429a172fe7abca59`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 17 Feb 2026 22:08:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 17 Feb 2026 22:08:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 17 Feb 2026 22:08:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Feb 2026 22:08:02 GMT
ENV CLOJURE_VERSION=1.12.4.1602
# Tue, 17 Feb 2026 22:08:02 GMT
WORKDIR /tmp
# Tue, 17 Feb 2026 22:08:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "61a43afdb55328e75b7a4752960c8c353755a5a2e3a4c485cca2e3ac92481138 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 17 Feb 2026 22:08:43 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 17 Feb 2026 22:08:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 17 Feb 2026 22:08:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:4c4c4621da5085342b3b0d8d8ef57e5e44004eedf5818268af30c41a02cb6cf2`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 47.1 MB (47138343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51e535dc0d305223a844c3403214deb9ebadafbe1230d72a59516621edab4af`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 135.6 MB (135627120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fac0f3438fb97703862fe1a360c7b738eb90b53b6e51b06e0b2272d9fbb62b`  
		Last Modified: Tue, 17 Feb 2026 22:09:26 GMT  
		Size: 80.0 MB (79963630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8114ff17ded5acf65b5581f501b987e1b76658799eb9188554c74eeb998ef5c`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79abe58c641c1e3a0f2c104e5649d172ff01c9c0f6d1279e1919793db821c56a`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:fd4e247b80f8fb28c4e27017ed3d7d3dba08dcd2af185b4191bd8545f091a132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7383886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28f6c85533d5fa0d9e6ad980be9d2f7e578b608784c7da77c012b980bf3695a`

```dockerfile
```

-	Layers:
	-	`sha256:b644b3b80d5f0bef719e809e570ca8f4f4f5b3337ab06bdef33569111b7146d0`  
		Last Modified: Tue, 17 Feb 2026 22:09:24 GMT  
		Size: 7.4 MB (7368108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9838ed0d57a15449de1a5e7917a5ed736b6303ed966955ad2a742b0a5d62d43`  
		Last Modified: Tue, 17 Feb 2026 22:09:23 GMT  
		Size: 15.8 KB (15778 bytes)  
		MIME: application/vnd.in-toto+json
