## `clojure:temurin-25-bullseye`

```console
$ docker pull clojure@sha256:c335e69a26411b4d3c0df4e1fecdf699a0d757545cf541ecbdcf887263911903
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a2eabcbcc1569fce68c3135c9f8d7a0a37b6c52c68817fe3465d45c5d8ceb79d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.6 MB (215621456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a86d6012bbdea7f23d743acd7044504bc857f22f6c0acc0d6dbad92cc133283`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:06:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:06:44 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:06:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:06:44 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:06:44 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:06:57 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:06:57 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:06:57 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b47c027ad0f47e2002261dd2e82a36c096ae4f0c969b6056351ca1a23f02e3d`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 92.3 MB (92256319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510e84f309e797c15fdeea4645c9dbbe236e13030271be8d2bbc442644bb7f85`  
		Last Modified: Wed, 15 Apr 2026 22:07:18 GMT  
		Size: 69.6 MB (69601299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c5529f4387a1dcc4e15a03201082aa29c27434fd6c8a76f7819ce236f4a151`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba76cd141a7d6de05e80fcd5fb50c2e7ba25be79387fe9adb9945c41c3585fa6`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:f1d64ddc5312be464b3ab24a2599a9332872f82080be373ddb2d4a68b3ad3c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae28e2343276f766a9fa2265594ea19504cfa643cceb618c039ae0f8cc680d15`

```dockerfile
```

-	Layers:
	-	`sha256:319072fc4709640f3d78e1a37bb91a0980e26e3f42ae9410ba486f0148ba86c6`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 7.4 MB (7375727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a101fd47559ec2be10efaca46807c5c62d3520e52ae1e8b2f23ae286b0d4019a`  
		Last Modified: Wed, 15 Apr 2026 22:07:14 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:0d3df63c084c1ef4c9ef6c6ec0c0edafd9543d5398d994fe3570f69d34fbb56d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.3 MB (213272942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93fc0cdffe75aab616cb311f0cc71e427b529b35104df6d4e8b8912f1a294e8a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:18:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:18:23 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:18:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:18:23 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:18:23 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:18:37 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:18:37 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:18:37 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 15 Apr 2026 22:18:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 15 Apr 2026 22:18:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c87149bbc094da1503aa0ed4a2b2c73c997792d3c279a52b7505fa497287c1fe`  
		Last Modified: Wed, 15 Apr 2026 22:19:00 GMT  
		Size: 91.3 MB (91288275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480732404db3cc38da23d085fff9ab20e8ad31bfd2189a3e5feea92725343a4c`  
		Last Modified: Wed, 15 Apr 2026 22:19:00 GMT  
		Size: 69.7 MB (69736010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9078676262695adfd5bd30e650c51d972a8f5be731e455915d000b5ea9bf3ff8`  
		Last Modified: Wed, 15 Apr 2026 22:18:57 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2871283ccc0404cf815e3b07885a285fc607d540d3a36557b0d61035230022`  
		Last Modified: Wed, 15 Apr 2026 22:18:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4e703c3ec8591acdebed67b50519592ccdf9c10ce4da3fefe90126e191147acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7397436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1341b1b532ae62d24955f879f6fc072c1599c08a256e283cec8ca0ccbb70b9`

```dockerfile
```

-	Layers:
	-	`sha256:7bab7e7e8065a7006a7f403f8ccce1d3607ee7c2f38018f96eb0b6d65c8ae807`  
		Last Modified: Wed, 15 Apr 2026 22:18:57 GMT  
		Size: 7.4 MB (7380847 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d630a2cac8ce9fc7c379c398ab1fd9d623523fe2943951be7123e9be579e5554`  
		Last Modified: Wed, 15 Apr 2026 22:18:56 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
