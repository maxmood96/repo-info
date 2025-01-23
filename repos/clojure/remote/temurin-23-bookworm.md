## `clojure:temurin-23-bookworm`

```console
$ docker pull clojure@sha256:6ae1b01a3865075d73624f36224308b5196ffda1ea5e08d8b5ef10880ce6b692
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8165847fb15729b15b3ef18d9a4764194d8b17872e01e3e4e35f64dc53a22c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294754129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241634231b3fd6069caaf235288190c5a56ef2650153360180198f9cdd05a6cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d28fd6b84cfc70c68d96a9b46dc89d01b286afa28d3d77b93f863652142d22f`  
		Last Modified: Wed, 22 Jan 2025 19:42:34 GMT  
		Size: 165.3 MB (165295134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4890fdaed54e8a94576856dd22f91b9540313265af9838380d715d7d96f672`  
		Last Modified: Wed, 22 Jan 2025 19:42:33 GMT  
		Size: 81.0 MB (80977989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5153e344e9d69c88433d1449f7d6171fff2bfdf8a44e08c5a3b3c11bd07015bc`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c948e6b543921be6ccd5c4d180ba917026fe3cc184abf3a1f1cfd7aff50c84b`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:65690afb4e5b3e4a1f90dc1d9b1c91ea048289a30d932267fe01e63c02f652fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7193273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e3a793b47d0e6b9c58695f4dab5fc11d1f9b8a065eaae0328d84d7eff04330c`

```dockerfile
```

-	Layers:
	-	`sha256:4ca1914e8628cd7145301aa456f2e4e2cb38c07bf4c1f406ae03c59434d8f11a`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 7.2 MB (7176769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a82a4dab03b58954b95fc62f9de43be7ee73301f60aeccd906036c78eb02d3a4`  
		Last Modified: Wed, 22 Jan 2025 19:42:32 GMT  
		Size: 16.5 KB (16504 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:743eea67847aef8684a92009543c26e4b608189c15544d219f8609260359e48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292416162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6742d357a9fb1a04f525c12597d4753d71532fbca779c70a68c7b31b9e115693`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 01:35:41 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4c88830c9b0ef7fe993d1c8ee9f25deaec3fe7c5624e05da6307d1c5dd1ab9`  
		Last Modified: Tue, 14 Jan 2025 12:39:01 GMT  
		Size: 163.3 MB (163281784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca87f4a0dfc6703d5506be0d99a37791e8e3dd5fe572ec6d664d95bb9d370923`  
		Last Modified: Tue, 14 Jan 2025 12:42:31 GMT  
		Size: 80.8 MB (80826444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89cd912e2c553beb4ca5e3217430106b450a07c59397624f2cacec0e7fb310dc`  
		Last Modified: Tue, 14 Jan 2025 12:42:29 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81c5adb7e5efb1d5c128aca5085082bc5c0ffa340035403aedd4e2a3535b482`  
		Last Modified: Tue, 14 Jan 2025 12:42:29 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e8c47d3bd28a7660761080e69b50600ea629a9e4cc01056c1d41ce3c83914d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7197781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675c2e84acba6f8ec73966ddb32af845ab595412806c1682e2619e19d722748a`

```dockerfile
```

-	Layers:
	-	`sha256:79313d39bc5069d3fb1e3fda2ea0c133f87cc98e9b9e7ac4fb3dde4bdcbfd5a8`  
		Last Modified: Tue, 14 Jan 2025 12:42:29 GMT  
		Size: 7.2 MB (7181935 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d98a81cd7f6960900752c5d410fbc72dc3203bc54ff13b4ad2776fd70c409c72`  
		Last Modified: Tue, 14 Jan 2025 12:42:29 GMT  
		Size: 15.8 KB (15846 bytes)  
		MIME: application/vnd.in-toto+json
