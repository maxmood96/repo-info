## `clojure:temurin-25-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9f7d0d97c16fe8559a554f3ff47b0c92783c969d1fd74565be1c9cca39bc2959
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4e51a1a894f40685b40447fa8eeacb64bdab73b19effc9b85e1f524fe335f5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **215.4 MB (215354741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc15ca7aee657975d6a78a39ee617cdb7a553da99cb37082ebd504d43167e784`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:56:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:56:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:56:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:56:34 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:56:34 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:56:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:56:48 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:56:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1e2d66c9d9f8efe285cc550f7cf8cb1194222debc79cfaec92fe8f171356abec`  
		Last Modified: Tue, 04 Nov 2025 00:13:02 GMT  
		Size: 53.8 MB (53756694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2594a5ba4350ffc1f3ed9380576b9280ec1f96083af48f8ed16fbc50ae647b`  
		Last Modified: Tue, 04 Nov 2025 00:57:20 GMT  
		Size: 92.0 MB (92036051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e9b938f092b3618e6013f1a23851bca38c8dc4ce8cc9f4d79db765c73b13b9`  
		Last Modified: Tue, 04 Nov 2025 00:57:19 GMT  
		Size: 69.6 MB (69560957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5800067697bc3f86b9561d94deb58740e9ea670cb32dc0b6a5efb6cbdda09af`  
		Last Modified: Tue, 04 Nov 2025 00:57:12 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e3c9bb15bc4529a375a7a5f52eb43307a83294ef998cbd773b6fdfc0ee9d269`  
		Last Modified: Tue, 04 Nov 2025 00:57:13 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:41728bb429d40368ee7cdc688fbc0a613f769fcad1a6b6a139c6050191ce7e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d91bc6448013139d256af39246141270a9288fe8186cd9975e4ce53b48d7bd2`

```dockerfile
```

-	Layers:
	-	`sha256:62d5d56490aa21cae39ba3016fb526f78b1d91701039fea0de5f4127503c417b`  
		Last Modified: Tue, 04 Nov 2025 10:45:38 GMT  
		Size: 7.3 MB (7346993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b790bce952facc8043a076a6234d5b429d1d199f09e9e8bad0f40183056208d`  
		Last Modified: Tue, 04 Nov 2025 10:45:39 GMT  
		Size: 16.4 KB (16447 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c6e3fcee34c7f27c03589e0bec57967efc36ece10f6ae7319d952a9e5ce2303f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (212992325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9e180c73e1a4822cfeaad37a6ce614e72e4050a5facf1443fe5d01e7356fe92`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1762202650'
# Tue, 04 Nov 2025 00:57:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 04 Nov 2025 00:57:31 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 04 Nov 2025 00:57:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 00:57:31 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Tue, 04 Nov 2025 00:57:31 GMT
WORKDIR /tmp
# Tue, 04 Nov 2025 00:57:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 04 Nov 2025 00:57:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 04 Nov 2025 00:57:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 04 Nov 2025 00:57:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 04 Nov 2025 00:57:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fd1e161a67e40ef9e2635aad60e4206efb76978ad46d67a3d4e7430236c982bf`  
		Last Modified: Tue, 04 Nov 2025 00:13:13 GMT  
		Size: 52.3 MB (52257969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436715c6425d29ea6f1967d61c53a17982a69185c713e6ef0545b36f6e0c2209`  
		Last Modified: Tue, 04 Nov 2025 00:58:29 GMT  
		Size: 91.0 MB (91045229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ace7378078f747b664aa52643f18a2a372c7e402dfd8bd5b781c5b6209da782`  
		Last Modified: Tue, 04 Nov 2025 00:58:21 GMT  
		Size: 69.7 MB (69688085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25957fb64e7341268f7ba4f4fa4e5ef180e96b37a94c81f8dcb3a70dc02bf49`  
		Last Modified: Tue, 04 Nov 2025 00:58:14 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02897468436cf9861732ede3913689acf6f824ba938874d6657e76cb8fa4f42c`  
		Last Modified: Tue, 04 Nov 2025 00:58:14 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4152fb5e31b2c40c0437525c50e30fc2567928e8e4ab260eab522be4b73b88a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7368702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfc784eab1d771baf2bf55158751b1f89d711f06067206bb0f3e8f97accca23`

```dockerfile
```

-	Layers:
	-	`sha256:864cd7ff6ffb80e414ad4848b09025e98f2f614afec5d891eb63086429bbb44c`  
		Last Modified: Tue, 04 Nov 2025 10:45:45 GMT  
		Size: 7.4 MB (7352113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:911cccc8e5bb250cf7ec8455ac09f282b13ddc2c329a986badfb5c638728063e`  
		Last Modified: Tue, 04 Nov 2025 10:45:46 GMT  
		Size: 16.6 KB (16589 bytes)  
		MIME: application/vnd.in-toto+json
