## `clojure:tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:95774898043a4b29adc4d9db8e18511778b468cef3bb53ce7f509151ec9afdd6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:c55cac5e9ba14bd6a3eaab80428163a9e34167d761fbecfb2d3fbe9c6d5835da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282995551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e16b4c29117604d0ade8d56c436753953efb8b226ba5a26de2116486044ea231`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967f6ef4dcc6fedfd2503f086ed3e863c0d0c87b5d880b3988eede06fb2d3dd7`  
		Last Modified: Fri, 27 Sep 2024 06:01:33 GMT  
		Size: 158.6 MB (158579256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ca6f97d3e31c704e982492ac32332e58414093eadd88f42123515235c24df3`  
		Last Modified: Fri, 27 Sep 2024 06:01:32 GMT  
		Size: 69.3 MB (69333866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c003167083670d226379525a944fd7a58c938fd66f9da4412f719532efbaa45f`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7b585b648dfe3991e63a55f37056742cebb021a7ed282760518be5298c4a164`  
		Last Modified: Fri, 27 Sep 2024 06:01:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:93816a25d618fcf4790c0f1520677c1f13b2e0c699f0a86936878f9b3fce118a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:025234132daabcbe75508e2b23dc53a9e43677368b2397e479185141cbe2c6ce`

```dockerfile
```

-	Layers:
	-	`sha256:996efd1446b1cc660b209deff945a760578677e86a245831317dfd6518f6a663`  
		Last Modified: Fri, 27 Sep 2024 06:01:30 GMT  
		Size: 7.2 MB (7193744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:325617d6ad9e8d4dc9aab26815d9c56508f30cfd3a56b42496b71ce41b79b049`  
		Last Modified: Fri, 27 Sep 2024 06:01:30 GMT  
		Size: 16.1 KB (16116 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dcdae825d53c33bbb01136551476de12441c5fb1baa8e7e5963cfbd7a9b01b69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279947754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ccf933035c204a0a12791ff004537cdfb2c3cf6d1b5e0b96ec1c5ac3e540ab8`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b635342920c0fcab5b69cf20eae9e783b6322a441926d40989856b1f74eb1c41`  
		Last Modified: Fri, 27 Sep 2024 10:41:12 GMT  
		Size: 156.7 MB (156746168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae22f516ad06a83817f94a576fa08c1ea87080e9f844dce50fba5b48127baa`  
		Last Modified: Fri, 27 Sep 2024 10:44:44 GMT  
		Size: 69.5 MB (69466687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3f3236173ec84923d8af92535df61040f47a02378b5b0e792bbf291651c76b`  
		Last Modified: Fri, 27 Sep 2024 10:44:42 GMT  
		Size: 608.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37c74636ab7ab05147fafdea27918f26dd89a808220a9a0512e3e3bb374e4a2`  
		Last Modified: Fri, 27 Sep 2024 10:44:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fcbe237980f51fd8a328ce4e827b85923259b214266b3ef3fd6be6b33015e425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10042959d4b6dc4a5b12e23349f444c15edd91c88fe582f057ca20f2c703542f`

```dockerfile
```

-	Layers:
	-	`sha256:db75821ab0243c64a0f8d5fd751040b245e3eaa116c342074c763728e4030adb`  
		Last Modified: Fri, 27 Sep 2024 10:44:43 GMT  
		Size: 7.2 MB (7198871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47222ef7fe5092273068747fba3d06619dda5d298eec803cc9663a2a417fd26d`  
		Last Modified: Fri, 27 Sep 2024 10:44:42 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json
