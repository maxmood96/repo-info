## `clojure:temurin-25-bookworm-slim`

```console
$ docker pull clojure@sha256:17b1e845bf105cce8ba3be6555f08dc5726d4d520b8a4112eb00c2a1d1510028
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

### `clojure:temurin-25-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:3ed865c79975060b1ca3f3646ce9b574d8da82d06869c1d793d38f8d00d48007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.2 MB (190192612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fab9dbeee57ffceca9402db8ccc049ae1ecee0ad7d35b8f3e1dc29c48e97ef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:20:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:20:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:20:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:20:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:20:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:21:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:21:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:21:10 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:21:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:21:10 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b940c5a0722435f1b01248646b8ef00a746b25a5dabb6c7326aab8c0c409a79b`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 92.3 MB (92256332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7572c8e05b05843f7b492531284b5693210b0c5acae8e753716f85c40b4f46`  
		Last Modified: Wed, 22 Apr 2026 02:21:31 GMT  
		Size: 69.7 MB (69698987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcffdefdeb69a2aeba1929c6585cba5694ecddc0375c744c1215d0196e4334fc`  
		Last Modified: Wed, 22 Apr 2026 02:21:28 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e954d2818afe96b816bf4c981188afd56e79b5a79eaf98ed9e9aec81d72088`  
		Last Modified: Wed, 22 Apr 2026 02:21:28 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:bb6625620682e5feafe0420c41d73dc1cc72b1a4ae4680a5ba4071b67903f26d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5100784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d69f3246cbfc399d7c6b6e357d418163e5d920ce730885462ccf9ff54c77a13d`

```dockerfile
```

-	Layers:
	-	`sha256:d49fbc22863db468866d3c2bb88356a685909bafdbd3973a93f60f154577709c`  
		Last Modified: Wed, 22 Apr 2026 02:21:29 GMT  
		Size: 5.1 MB (5084261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e4034c891926b0cbc1942d542e6c3c273924cd4b84a2d464bae402615edcc9`  
		Last Modified: Wed, 22 Apr 2026 02:21:28 GMT  
		Size: 16.5 KB (16523 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:cde2b85ea2fd8c17aa684750285d6d6acbcb721495c60d2355d959b6708c4bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.1 MB (189097545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37a0a12a8dba712d7c84a1f7e59089c7937f6b85b8033e88854b074919e1bee8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:23:55 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 02:23:55 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 02:23:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:23:55 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 02:23:56 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 02:24:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 02:24:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 02:24:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 02:24:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 02:24:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71e61d6cc84296320f757691e0c3d09752c315a06e57c9446f92649ac482b421`  
		Last Modified: Wed, 22 Apr 2026 02:24:34 GMT  
		Size: 91.3 MB (91288276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3fa3b0f1f2b27756ef9e35ebac28c37dab9ae4576a3b08d1014a0086cc2c992`  
		Last Modified: Wed, 22 Apr 2026 02:24:32 GMT  
		Size: 69.7 MB (69692117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c61dc2c40d0f7a74574092e23b1565cb833c1f4780b968980070a52472060c`  
		Last Modified: Wed, 22 Apr 2026 02:24:29 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27b3f90bcffd05bcbac685dcc09c1dc0e41486c770fbdf999303b2f3167b36`  
		Last Modified: Wed, 22 Apr 2026 02:24:28 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8701ea28e23b9cd6894599df62122ca2114fa197def56dbe85bc87c440d8a5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5106710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:742719c7b3ee570254ec3caa382ae4d0e33a3eba08af8c93d5885b1c3fc21ce4`

```dockerfile
```

-	Layers:
	-	`sha256:fa088b3890533ab88858aee52c0c568aa8602f7983d1f5f0b10b846d86fffcbd`  
		Last Modified: Wed, 22 Apr 2026 02:24:29 GMT  
		Size: 5.1 MB (5090043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57a0dd61b8240dc946ec707448e2d2208503cd889f20bc3a411ea09e8f452205`  
		Last Modified: Wed, 22 Apr 2026 02:24:29 GMT  
		Size: 16.7 KB (16667 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:2bb2e649e828fbe996377f318989288b6a282d728f31ffec0f57d3f1116dd2fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.2 MB (199242700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097a9869e4450d8a531a759abf03fd926ddcd70741a3dae6c4c7b186c8fd1d58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 08:44:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 08:44:51 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 08:44:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 08:44:51 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 08:44:52 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 08:48:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 08:48:40 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 08:48:40 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 08:48:40 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 08:48:40 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0bcb46f6315f7a2c8ddde875fca21de96c94e451046e6692f77a99aca489f3be`  
		Last Modified: Wed, 22 Apr 2026 00:15:02 GMT  
		Size: 32.1 MB (32078402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afb51c960e2b35dca8ff09367f059e4eede70dacb3d590bcc2a19c5e38fea02`  
		Last Modified: Wed, 22 Apr 2026 08:46:00 GMT  
		Size: 91.6 MB (91633101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcb42eba0c21d755738b751ab2d786fca1bf3fd3c53f2cc750241f55747a686`  
		Last Modified: Wed, 22 Apr 2026 08:49:14 GMT  
		Size: 75.5 MB (75530156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c26e43a49101e1a65e4c1dfb6198ccf93dca36a478729f63992e9117188abe`  
		Last Modified: Wed, 22 Apr 2026 08:49:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e649b22c977701b7ff10c321043a5daaa0191db9e7e7948e544f4b26956fe822`  
		Last Modified: Wed, 22 Apr 2026 08:49:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:017323082e08cc6eb1851b2818fb3686c9b446de3dd2a18521eb35bb0b4abc26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5089328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9226080e157293b976de16d4af09188ffc033c0652cb0db70ebc094eec5d905c`

```dockerfile
```

-	Layers:
	-	`sha256:234c97451099fddf9ec7871e01695b90644fbe68459cffbe8c94f71a898c7636`  
		Last Modified: Wed, 22 Apr 2026 08:49:12 GMT  
		Size: 5.1 MB (5072743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2d55e18da91325ba5ae54d0f6043c055f3a7d7eb9046bf738086b3e6c982a7e`  
		Last Modified: Wed, 22 Apr 2026 08:49:11 GMT  
		Size: 16.6 KB (16585 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:e48195233b382c2654a23b6277a838845db99720f66c31fba96c93db9854374e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.6 MB (183639260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42db7dea1485173977113c5c989585e76d2eb95f4113e4be841aa3401f6d57e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 04:04:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 22 Apr 2026 04:04:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 22 Apr 2026 04:04:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 04:04:57 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 22 Apr 2026 04:04:57 GMT
WORKDIR /tmp
# Wed, 22 Apr 2026 04:06:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 22 Apr 2026 04:06:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 22 Apr 2026 04:06:08 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 22 Apr 2026 04:06:08 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 22 Apr 2026 04:06:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e579a0e0e7bfecd47e7766cad04eb36ba4b3ee329c3806a48d41d336705a1ca6`  
		Last Modified: Wed, 22 Apr 2026 00:15:36 GMT  
		Size: 26.9 MB (26891563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe371a317b1e8d0173b45c71ab2e942734aba17edbcad4ca0dc90ba9f9057987`  
		Last Modified: Wed, 22 Apr 2026 04:05:36 GMT  
		Size: 88.2 MB (88233823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b64595610e87e556bcc687a5f1d77ef29c6f6dbc63d7d302a81b6a963e3d07d`  
		Last Modified: Wed, 22 Apr 2026 04:06:31 GMT  
		Size: 68.5 MB (68512835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c38c7c46d26e880643810e9b18ca55d7f723aaa3500d1e28a8550bdcf07e8f`  
		Last Modified: Wed, 22 Apr 2026 04:06:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6340f3095b4cdedcf045aa187f924ab16ccb9ed5f9371a68166c31383b20fb33`  
		Last Modified: Wed, 22 Apr 2026 04:06:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ad5920a4c10177cf90830f5c3d99b110dcecc5f988c6f78f117378184b028c27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5076669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:487c7f3bb8e28cb3f8a8a436902334fa261f26978d60219ba2e51ccf1ee25f95`

```dockerfile
```

-	Layers:
	-	`sha256:556fc1eaaea3e711968f9ef34fc3729a4729634ca31c55eb0a941e8cb95cf84c`  
		Last Modified: Wed, 22 Apr 2026 04:06:30 GMT  
		Size: 5.1 MB (5060144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b6ed7bdfad69dc627b97d1ffdc5235f57e825b0209e8da48e58d5cd3c59a71a`  
		Last Modified: Wed, 22 Apr 2026 04:06:29 GMT  
		Size: 16.5 KB (16525 bytes)  
		MIME: application/vnd.in-toto+json
