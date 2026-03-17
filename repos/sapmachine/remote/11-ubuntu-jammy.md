## `sapmachine:11-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:b039c285f933b9a62fddd1727849cb776534ec4c902973cb1e4a9b44d559786e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:580cd36f6c7ac2674e062cdf640962fd9321fbff26cf108a8aec8fd92390ce16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.8 MB (229845397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5a4aadf58c343f345b587854ab31864fd2514864b8099be50885f5a2ed55977`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:26:25 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.30 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:26:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 17 Mar 2026 02:26:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6415ec47aa78af7b36308555123b11c7374bbeacbb4a596bb3585d62c4eaad85`  
		Last Modified: Tue, 17 Mar 2026 02:26:48 GMT  
		Size: 200.3 MB (200306877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:28e9c91bf521487c4e450339c0d88928d6f351764ac09e39658b85738cd9c343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2650722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b63d237ca2728bb7f7fec255ea6ad3dfd8fd3a274f0feb0438fc270308c3dbc`

```dockerfile
```

-	Layers:
	-	`sha256:a0216a22ef88062d4a37bfd7bdcfdeb90a990ffde31efa975c2358d6a653ea0b`  
		Last Modified: Tue, 17 Mar 2026 02:26:43 GMT  
		Size: 2.6 MB (2640627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ce17659aca6ebd8d3ad3b62b951e875468cee495d9ce43368ed7bc5f0807cbf`  
		Last Modified: Tue, 17 Mar 2026 02:26:43 GMT  
		Size: 10.1 KB (10095 bytes)  
		MIME: application/vnd.in-toto+json
