## `clojure:temurin-22-tools-deps-1.11.4.1474-bullseye`

```console
$ docker pull clojure@sha256:8fe70fc1185701c5a79900172499d6ab7ef22f26ba773720b8a9b16ab8ec85ae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-1.11.4.1474-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4ceff5d02ee256c7f34033ef8343586e1cc515c13136aa49ec4b67683839c9c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.5 MB (280529646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d43d331952c9b07d2f21d1ab6d7be319706bbc4ecf4518054eb4688c94d6948a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:6648a8158bbf4a36244eb9e936fbed4ea29f2f090fb0a97a6a737be2d85a5333 in / 
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
	-	`sha256:203e9cf21bd27322e5baf32653bf3314ccf688be497585240d18b9f0ca24f2ee`  
		Last Modified: Tue, 13 Aug 2024 00:24:05 GMT  
		Size: 55.1 MB (55084675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855dfeb5f912c85fec6c98d073fd1e2669b3058036bb1b93f263e369fe55f563`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 156.5 MB (156481638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e354995cab361ead6fdd6317b04d9a2b48007f06df40ebc5ac9de57df7540bef`  
		Last Modified: Sat, 17 Aug 2024 02:04:30 GMT  
		Size: 69.0 MB (68962293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ff53633d96b0d85fc4d588c9d48a9762e95332e3f7fac9e443ee2569fdac5a`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd94a039ef26c7bfad13abc75f7e2c52d750ec794c4a9e4929380836fde0a661`  
		Last Modified: Sat, 17 Aug 2024 02:04:27 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a2d51b8032275933f7a1782d51098b82c71e3449f11f8ecf9d4ebee781c194f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7055778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:926070b6120ebb6c58d3b5955651145fcd378cbe9b0a0ba196a7713a026078f0`

```dockerfile
```

-	Layers:
	-	`sha256:145d514a38878d420fd70996e103071fb30d7bc6df26851897b5bb48b4e4e3a6`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 7.0 MB (7040338 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bad4d54978d8cd9fb55bdf95f2e82bd4a0fe8236a3edded061cb3797bc59caa8`  
		Last Modified: Sat, 17 Aug 2024 02:04:29 GMT  
		Size: 15.4 KB (15440 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-1.11.4.1474-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e77f866a77f75150e77084c385adcbc6dbddafce43fdea9e42977cc6f0c31308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.3 MB (277324842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaec5ceaa34c782c0f58b958fdc0b670e495ec7d47f311da75c6b1f1357d440`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
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
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c773b2f891a201a4c6dbf89d20c0c5d9f30e6850dc290d042e4937ad3128e1`  
		Last Modified: Tue, 13 Aug 2024 06:46:25 GMT  
		Size: 154.5 MB (154503731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2d6e6834158921e71d3347ba4ca4ddff64a16bbac9a63f3023cd44f23dddc1`  
		Last Modified: Tue, 13 Aug 2024 06:49:45 GMT  
		Size: 69.1 MB (69090149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6b0b66a82c2d6eef2da6a5f9299860d0508a6e7a6fabbe55c3b5789f4af42`  
		Last Modified: Tue, 13 Aug 2024 06:49:43 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07032cf30194714ded2a8e9cefa725713cc5d227bd4783e244293c492ac5f418`  
		Last Modified: Tue, 13 Aug 2024 06:49:43 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-1.11.4.1474-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:240e13d96ea37e3559d72d304d38eaf276e0d115f5910bf9dcdf48c7118ebe24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7062036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0663b4414d15642a05e97754c0c7a84b1493a86e56d59a0de28af6bee66581f2`

```dockerfile
```

-	Layers:
	-	`sha256:1d4086d925b1e5efd75ffd8439789b18f0c379fd4c1d02f9d3794b41ae6b1983`  
		Last Modified: Tue, 13 Aug 2024 06:49:44 GMT  
		Size: 7.0 MB (7046060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:403ddb0e2a4206635d6996e42387612edef1cd2f453e6c0901b4a240db5a0923`  
		Last Modified: Tue, 13 Aug 2024 06:49:43 GMT  
		Size: 16.0 KB (15976 bytes)  
		MIME: application/vnd.in-toto+json
