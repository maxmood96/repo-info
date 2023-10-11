<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `couchdb`

-	[`couchdb:2`](#couchdb2)
-	[`couchdb:2.3`](#couchdb23)
-	[`couchdb:2.3.1`](#couchdb231)
-	[`couchdb:3`](#couchdb3)
-	[`couchdb:3.1`](#couchdb31)
-	[`couchdb:3.1.2`](#couchdb312)
-	[`couchdb:3.2`](#couchdb32)
-	[`couchdb:3.2.3`](#couchdb323)
-	[`couchdb:3.3`](#couchdb33)
-	[`couchdb:3.3.2`](#couchdb332)
-	[`couchdb:latest`](#couchdblatest)

## `couchdb:2`

```console
$ docker pull couchdb@sha256:f6267f17bf5e70c1b25ecc13f46e6cc464c4f21ede52c7a3449e0c753d67c63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2` - linux; amd64

```console
$ docker pull couchdb@sha256:f54909299527fd45e8512518b97d47931aa12bde4012ecb5813b49705b000e28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca6b7f818e098f2b9242f55e5d001342cef6ad0016e914745a9fb941cbea292`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:41:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:41:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Sep 2023 07:41:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:41:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:42:05 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 20 Sep 2023 07:42:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:42:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:42:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:42:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:42:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 20 Sep 2023 07:42:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:42:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:42:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:42:25 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:42:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5339bae7194fb6787f979a78e790921ea71a198c722add3f2b014dd06a37b7d`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33dff033631360b0277f9d704c9a7aa2d427f70315a3adf7ca8788e71f097c7`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 6.7 MB (6704607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60de85677f42aee612a87ecc31fb26b473f15d20af2e4011d37a716fe889f2`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 1.3 MB (1259896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794235488f03eb10f081f12179fa3fb036d9d52d8a0664b51430318522ba5e40`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 294.6 KB (294602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413059af153813468ad4cf75503fb45edea536569000014db67fb092e89bd4f`  
		Last Modified: Wed, 20 Sep 2023 07:43:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179ab28c9d828f43c6e730974cb53e0031576008675f929172c3ba217fbe371`  
		Last Modified: Wed, 20 Sep 2023 07:43:34 GMT  
		Size: 49.1 MB (49137306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6121a5562f211664c28ea91d39f516ccd16c32334bc92dbdb601a2000abd3`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619239618e41bf5adf90ac645a869b9b6d473d11b34ee2c641f3ef0f2de09e1`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a2e85355a29b02dced3b25d167f2e3b54f2e304a613eab798fc9da08d602`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9caf8bc2e9f7fe8ea47cfb9ebb810b878dee135b81fc007ca3dd9c2cbf0d56`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:99e33ca3612dbd4695a96cf9591d29cc61d2d3dcf9593ed14ced05404178e04b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73042217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630b66eaaeab61debcbacc65de2fc5bb65dd180d5dddfaa923c5bc31257ea2ad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:21 GMT
ADD file:013dd6e1187d63722cbaddc725f44bc6789ce42a75e2ae86456088763728139c in / 
# Wed, 11 Oct 2023 18:25:21 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:02:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:02:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:02:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Oct 2023 20:02:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:34 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Oct 2023 20:02:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:02:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:02:46 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:02:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:02:47 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Oct 2023 20:02:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:02:47 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:02:47 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:02:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:466d0c81a91b4dea612f4d4bcbd480b8ee299558a2d50e93104c98a012e7975e`  
		Last Modified: Wed, 11 Oct 2023 18:29:47 GMT  
		Size: 26.0 MB (25967816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d44b3c33bdf895337d17dca5816d4d9daa7d71012220aa038a5693b8794941`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b2740e8143dadd14b66ec7c7289c2c5e75e90163dbee383fad72cf89e79f4f`  
		Last Modified: Wed, 11 Oct 2023 20:03:32 GMT  
		Size: 6.6 MB (6577680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137382532f0542c42cb84e1a5fdcdcb13504bda5718de5fd570c130bde44b664`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 1.2 MB (1164827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b9f77d1d946a7812c227419e9b8818b110541b49879ec86db3ef26ed7c735`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 294.4 KB (294432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b17ed664da2686c7b24b4c1a15f59fe9e2b4aeb1d3679a9eaa0fe393e2abe2`  
		Last Modified: Wed, 11 Oct 2023 20:03:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c10e1c95e53c4bfcc2567b81476dbd378a940742eb6c9242abe86d94e849637`  
		Last Modified: Wed, 11 Oct 2023 20:03:46 GMT  
		Size: 39.0 MB (39030433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c926efaac26dd8726e3b1668fa906a9adab9fca884c44f11449ce3e14050683`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad9a247a78923da0dfcfcec98a27384e05b455b5738d02012a484b160216709`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76156cae3d35d088cdba79b2f121419b85c0d12ea4ceb4b2f932366d834978f`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7821f2debfd87f0ba936ee29f3c95ad7ce94c3232058d4f5f28a72a4cf5be4`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3`

```console
$ docker pull couchdb@sha256:f6267f17bf5e70c1b25ecc13f46e6cc464c4f21ede52c7a3449e0c753d67c63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:f54909299527fd45e8512518b97d47931aa12bde4012ecb5813b49705b000e28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca6b7f818e098f2b9242f55e5d001342cef6ad0016e914745a9fb941cbea292`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:41:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:41:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Sep 2023 07:41:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:41:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:42:05 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 20 Sep 2023 07:42:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:42:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:42:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:42:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:42:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 20 Sep 2023 07:42:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:42:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:42:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:42:25 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:42:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5339bae7194fb6787f979a78e790921ea71a198c722add3f2b014dd06a37b7d`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33dff033631360b0277f9d704c9a7aa2d427f70315a3adf7ca8788e71f097c7`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 6.7 MB (6704607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60de85677f42aee612a87ecc31fb26b473f15d20af2e4011d37a716fe889f2`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 1.3 MB (1259896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794235488f03eb10f081f12179fa3fb036d9d52d8a0664b51430318522ba5e40`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 294.6 KB (294602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413059af153813468ad4cf75503fb45edea536569000014db67fb092e89bd4f`  
		Last Modified: Wed, 20 Sep 2023 07:43:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179ab28c9d828f43c6e730974cb53e0031576008675f929172c3ba217fbe371`  
		Last Modified: Wed, 20 Sep 2023 07:43:34 GMT  
		Size: 49.1 MB (49137306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6121a5562f211664c28ea91d39f516ccd16c32334bc92dbdb601a2000abd3`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619239618e41bf5adf90ac645a869b9b6d473d11b34ee2c641f3ef0f2de09e1`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a2e85355a29b02dced3b25d167f2e3b54f2e304a613eab798fc9da08d602`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9caf8bc2e9f7fe8ea47cfb9ebb810b878dee135b81fc007ca3dd9c2cbf0d56`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:99e33ca3612dbd4695a96cf9591d29cc61d2d3dcf9593ed14ced05404178e04b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73042217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630b66eaaeab61debcbacc65de2fc5bb65dd180d5dddfaa923c5bc31257ea2ad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:21 GMT
ADD file:013dd6e1187d63722cbaddc725f44bc6789ce42a75e2ae86456088763728139c in / 
# Wed, 11 Oct 2023 18:25:21 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:02:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:02:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:02:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Oct 2023 20:02:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:34 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Oct 2023 20:02:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:02:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:02:46 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:02:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:02:47 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Oct 2023 20:02:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:02:47 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:02:47 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:02:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:466d0c81a91b4dea612f4d4bcbd480b8ee299558a2d50e93104c98a012e7975e`  
		Last Modified: Wed, 11 Oct 2023 18:29:47 GMT  
		Size: 26.0 MB (25967816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d44b3c33bdf895337d17dca5816d4d9daa7d71012220aa038a5693b8794941`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b2740e8143dadd14b66ec7c7289c2c5e75e90163dbee383fad72cf89e79f4f`  
		Last Modified: Wed, 11 Oct 2023 20:03:32 GMT  
		Size: 6.6 MB (6577680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137382532f0542c42cb84e1a5fdcdcb13504bda5718de5fd570c130bde44b664`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 1.2 MB (1164827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b9f77d1d946a7812c227419e9b8818b110541b49879ec86db3ef26ed7c735`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 294.4 KB (294432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b17ed664da2686c7b24b4c1a15f59fe9e2b4aeb1d3679a9eaa0fe393e2abe2`  
		Last Modified: Wed, 11 Oct 2023 20:03:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c10e1c95e53c4bfcc2567b81476dbd378a940742eb6c9242abe86d94e849637`  
		Last Modified: Wed, 11 Oct 2023 20:03:46 GMT  
		Size: 39.0 MB (39030433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c926efaac26dd8726e3b1668fa906a9adab9fca884c44f11449ce3e14050683`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad9a247a78923da0dfcfcec98a27384e05b455b5738d02012a484b160216709`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76156cae3d35d088cdba79b2f121419b85c0d12ea4ceb4b2f932366d834978f`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7821f2debfd87f0ba936ee29f3c95ad7ce94c3232058d4f5f28a72a4cf5be4`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:2.3.1`

```console
$ docker pull couchdb@sha256:f6267f17bf5e70c1b25ecc13f46e6cc464c4f21ede52c7a3449e0c753d67c63b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:2.3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:f54909299527fd45e8512518b97d47931aa12bde4012ecb5813b49705b000e28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84590831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca6b7f818e098f2b9242f55e5d001342cef6ad0016e914745a9fb941cbea292`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:41:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:41:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Sep 2023 07:41:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:41:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:42:05 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 20 Sep 2023 07:42:06 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:42:23 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:42:24 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:42:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:42:24 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 20 Sep 2023 07:42:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:42:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:42:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:42:25 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:42:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5339bae7194fb6787f979a78e790921ea71a198c722add3f2b014dd06a37b7d`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33dff033631360b0277f9d704c9a7aa2d427f70315a3adf7ca8788e71f097c7`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 6.7 MB (6704607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60de85677f42aee612a87ecc31fb26b473f15d20af2e4011d37a716fe889f2`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 1.3 MB (1259896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794235488f03eb10f081f12179fa3fb036d9d52d8a0664b51430318522ba5e40`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 294.6 KB (294602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3413059af153813468ad4cf75503fb45edea536569000014db67fb092e89bd4f`  
		Last Modified: Wed, 20 Sep 2023 07:43:30 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7179ab28c9d828f43c6e730974cb53e0031576008675f929172c3ba217fbe371`  
		Last Modified: Wed, 20 Sep 2023 07:43:34 GMT  
		Size: 49.1 MB (49137306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e6121a5562f211664c28ea91d39f516ccd16c32334bc92dbdb601a2000abd3`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2619239618e41bf5adf90ac645a869b9b6d473d11b34ee2c641f3ef0f2de09e1`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a2e85355a29b02dced3b25d167f2e3b54f2e304a613eab798fc9da08d602`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 2.1 KB (2056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9caf8bc2e9f7fe8ea47cfb9ebb810b878dee135b81fc007ca3dd9c2cbf0d56`  
		Last Modified: Wed, 20 Sep 2023 07:43:28 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:2.3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:99e33ca3612dbd4695a96cf9591d29cc61d2d3dcf9593ed14ced05404178e04b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.0 MB (73042217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630b66eaaeab61debcbacc65de2fc5bb65dd180d5dddfaa923c5bc31257ea2ad`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:21 GMT
ADD file:013dd6e1187d63722cbaddc725f44bc6789ce42a75e2ae86456088763728139c in / 
# Wed, 11 Oct 2023 18:25:21 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:02:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:02:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:02:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Oct 2023 20:02:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:34 GMT
ENV COUCHDB_VERSION=2.3.1-1
# Wed, 11 Oct 2023 20:02:34 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:02:46 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:02:46 GMT
COPY --chown=couchdb:couchdbfile:74a26e2e31f9b408e93e4a065004a86e00211d06a4ce6ab1fbc23640bd92a929 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:02:47 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:02:47 GMT
COPY file:a03eff89f810529ca878388de0c227b20fb661957d2117d1664d535138fc12e6 in /usr/local/bin 
# Wed, 11 Oct 2023 20:02:47 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:02:47 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:02:47 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:02:47 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:02:47 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:466d0c81a91b4dea612f4d4bcbd480b8ee299558a2d50e93104c98a012e7975e`  
		Last Modified: Wed, 11 Oct 2023 18:29:47 GMT  
		Size: 26.0 MB (25967816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d44b3c33bdf895337d17dca5816d4d9daa7d71012220aa038a5693b8794941`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b2740e8143dadd14b66ec7c7289c2c5e75e90163dbee383fad72cf89e79f4f`  
		Last Modified: Wed, 11 Oct 2023 20:03:32 GMT  
		Size: 6.6 MB (6577680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137382532f0542c42cb84e1a5fdcdcb13504bda5718de5fd570c130bde44b664`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 1.2 MB (1164827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b9f77d1d946a7812c227419e9b8818b110541b49879ec86db3ef26ed7c735`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 294.4 KB (294432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b17ed664da2686c7b24b4c1a15f59fe9e2b4aeb1d3679a9eaa0fe393e2abe2`  
		Last Modified: Wed, 11 Oct 2023 20:03:44 GMT  
		Size: 274.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c10e1c95e53c4bfcc2567b81476dbd378a940742eb6c9242abe86d94e849637`  
		Last Modified: Wed, 11 Oct 2023 20:03:46 GMT  
		Size: 39.0 MB (39030433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c926efaac26dd8726e3b1668fa906a9adab9fca884c44f11449ce3e14050683`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad9a247a78923da0dfcfcec98a27384e05b455b5738d02012a484b160216709`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 760.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76156cae3d35d088cdba79b2f121419b85c0d12ea4ceb4b2f932366d834978f`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7821f2debfd87f0ba936ee29f3c95ad7ce94c3232058d4f5f28a72a4cf5be4`  
		Last Modified: Wed, 11 Oct 2023 20:03:42 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3`

```console
$ docker pull couchdb@sha256:2d7c9bacbe4999d427b833a3066a9e785bb72da38e3a3af1e1788d8841f87efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3` - linux; amd64

```console
$ docker pull couchdb@sha256:e4c237b2cbc8dcaf41ac318d04e398be685c1eb6687720250f108bccafe61f1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78991f849f8c06f9274ce87618c10744071db6c4de7f7e1bedca1ac6e624789e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:40:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:40:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 07:40:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:40:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:45 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 07:40:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:40:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:00 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:41:00 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:41:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d8dff97665ef4ac74b8ba8b6ce7c6dacc5cfd8685014d8ae7c8f7feaf446e`  
		Last Modified: Wed, 20 Sep 2023 07:42:43 GMT  
		Size: 3.4 KB (3403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce890f4609ba4a6fb1db704f669081b13ba9e73efdcf8ab7ff9def4626c87f`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 5.2 MB (5224541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da104612da233e62f2e400c248c0ed004b6bf438d7fcc0dff894e0fb902a6132`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 610.3 KB (610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059880c0330e5a561bf01de9c2237fe79d400edf3e7f03542441fec49507f4`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 294.4 KB (294416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1aa965151c59ad7ac1ad873917848dfee3bdb4812dff9dec0ad409eb2604d8`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02984bcb5a695b4453285847308fa479e6c7eee775b2201fa524ddef8f084729`  
		Last Modified: Wed, 20 Sep 2023 07:42:44 GMT  
		Size: 52.7 MB (52685948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41d7eccab181e399d849912c788f6b8276835df0ba0aeaccc58c07517c39ed9`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4034a7db24e022618eff0e254c6dca735a41cf0024fe7f5cb9f005aac47a7b0`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a600c5fcec0d826f6ebea99e6d9d398ec0f65ab75770b1a77da0b3f60cf833`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bd6ec842fabe6e46b865a146d73a63be473c599e6d82af73a63682feca38ae`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b85e8329747a0bbe733b8c3625920b201478af047193fbc943a1c5571238500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88693275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253383c99318d7ad9a6831c541446261470e5f562dcbea09010b2a0a0e3ef53d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:01:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:01:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:01:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 20:01:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:29 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 20:01:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:01:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 20:01:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:01:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:01:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:01:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:01:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419fa3b20618be35a50656b826eb7bfdde4ef2946317c30c5a3768b38aaa8ba0`  
		Last Modified: Wed, 11 Oct 2023 20:03:05 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a80ec2d98f312cdb02ba63d1a882ab37247fb58659ffe8c2700fb74d2a0eea5`  
		Last Modified: Wed, 11 Oct 2023 20:03:04 GMT  
		Size: 5.2 MB (5210867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0fc376ff63452715c9a8a69338dfdf760491280c2e07909a6682afa27d7121`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 567.1 KB (567072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f7a37f661d9c02365eaf3dbe656c3838a0e3370364cbbc1096e5dd70a0c556`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 295.0 KB (295039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3f9f740e76573fa14868cc22c22cff8c24a6de99120e929a99dc13745da54`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a6ba63731db2ab523a856c11b65978f813bc44c0d24954d701204294de119`  
		Last Modified: Wed, 11 Oct 2023 20:03:06 GMT  
		Size: 52.5 MB (52548769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34294d7475990a1c770f8b0c00af4539f2679bd7b16d8299f6576e70a857bed`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa696bb2506cebba21d95ad6e5f7241fad9de808e98357c0061cf006dadde21d`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3bc6d83499278d2ea489a21230ef90bc400cc5e0e287a4d0efa21a67941821`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91b43446d8c1a3e1c5a14fb64012f452471ee6d253d1d9a4fecbe60dbcc3662`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f7bb9c90ca134dbb51470a71db984c40f76ee21040d37a7a83b570686eed9ad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604f3d59348c58a7dfcb181de5a4796da3efed1ac69dfb7811485cce6c53bc79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:11:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 18:11:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 18:11:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:11:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 18:11:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 18:12:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:12:03 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 18:12:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 18:12:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 18:12:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 18:12:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 18:12:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 18:12:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 18:12:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 18:12:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e790e2c9287694cf9652eb7c41d4826d2dd6355c09e0bf59368ce65009d14`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86edb71aa1531785c515ce961dc9adb23fe3cc93985ad5e2726cf09a9b22cdbf`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 6.0 MB (6046190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbee737be9f30885e44eb893e1016c499cea97cc3c25da02f0acbcd2426f5ae2`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 662.9 KB (662896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03258e5c9f472db9db19a9f68f553c696d7ad308c231a1cdea3524d4cd23678f`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 295.1 KB (295078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b635d512183aec2620576e59c565a891c5c1d545d9cce53ab979f8597c55034f`  
		Last Modified: Wed, 11 Oct 2023 18:13:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b905e7ba03087226b54c39e94e6494a0d4b878aba24d0fe83b1dd1ae88edb`  
		Last Modified: Wed, 11 Oct 2023 18:13:36 GMT  
		Size: 53.7 MB (53663080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8107b2ab7e005312a17c61ad4aabba919c479a1976ebc229b6bfc31c71d94fab`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ff9978944af4317513c68ca373b634280fade1b102d2ec40be616116f7158`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388947061f22f9094e8f2119f222e93e980faea84d73328a0d057f22fe026ff4`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e39de32eeee3db27f768655cdb1570e02a2cec7c7e3a87753acc8bf68f4293`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3` - linux; s390x

```console
$ docker pull couchdb@sha256:9f548cfa416c33e911c223dd11709138cabe43e0e5574f11a621a46b6fbf95a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86993125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592ecdc083e910a2759c594277924f9706573e2afb7a81aae1a6badea2a214b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 10:29:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 10:29:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 10:29:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 10:29:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 10:29:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:18 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 10:29:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 10:29:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 10:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 10:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 10:29:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 10:29:39 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 10:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309ebc55f4ef0cc6e5e6ff20c9e9865ff91632cfa7ec0e587ef781f92a575015`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb7d6b9954c9f37886cdb50b5641d3c61a70ee2b6ebfb00f1a62b17c1a9cdf2`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 5.1 MB (5110402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a1f2e24600d89783f110705b3c4da1812b439bfdc97e7fe4ac30a03ff0cd59`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2fc94dec365b1230ce01b2ba97657b0592d9c53524b031f72071a5a8b3502`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04c13697bb058424f77759f7e28422f4211699c6789c0555dc8355c2df1d0b`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f2fb5ff9494e91ccda88ccc3bf6a22cef8aabbac01b5959791452ec5d2abc`  
		Last Modified: Wed, 20 Sep 2023 10:29:55 GMT  
		Size: 51.4 MB (51354753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c87e354d6bb736d51b75fbab317c69a91f5ba5cc90e4b62c46c920c98db62a`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c933d81f71df9060221fd99d82a101ecf0f1c855b16fb3755bcf94962641b6`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7500a42ce1c25636182c530deddd254dd05a5d92eb343414b028e20e1b41476`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5269f1974cdaa958341c635ad403fe18b4c525fa3dceaddd3806106e041b3e2`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1`

```console
$ docker pull couchdb@sha256:7b3dd1a025f8822045e8b1d7d21bb501df86ca69a520c90f1b1689ec9a41735f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1` - linux; amd64

```console
$ docker pull couchdb@sha256:4b0621c760955c141e004c5aad11436b5e8da28732e6fc82eafb17b0b7563b6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80075301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da47e2251aaf06ffd73ae2a545a48d8c5f3555efb6e2ecd45f52bfe0ef7360c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:41:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:41:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Sep 2023 07:41:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:41:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:44 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 20 Sep 2023 07:41:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:41:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:41:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:41:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:41:59 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:42:00 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:42:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5339bae7194fb6787f979a78e790921ea71a198c722add3f2b014dd06a37b7d`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33dff033631360b0277f9d704c9a7aa2d427f70315a3adf7ca8788e71f097c7`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 6.7 MB (6704607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60de85677f42aee612a87ecc31fb26b473f15d20af2e4011d37a716fe889f2`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 1.3 MB (1259896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794235488f03eb10f081f12179fa3fb036d9d52d8a0664b51430318522ba5e40`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 294.6 KB (294602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8ad350c4e5f720f913387118e99041e592baeb703b502b75913bab3f5ae0c`  
		Last Modified: Wed, 20 Sep 2023 07:43:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4477cceb3e1a45db30b462264e8b6d1b3280de8a5a16b9a835b08b215cfaa80f`  
		Last Modified: Wed, 20 Sep 2023 07:43:19 GMT  
		Size: 44.6 MB (44621774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e960e8b538e8d6d311da0ac721fc3307a89309b3604e58f8f45df11686d97c3`  
		Last Modified: Wed, 20 Sep 2023 07:43:15 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ede81fe511bbc6234d3cd5f3557208a0058f739ad4fec9a189f300f88307219`  
		Last Modified: Wed, 20 Sep 2023 07:43:14 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e4cc476b00bc9fc56fc7ecc01fab98ff14c8415e5c5e0d81177d13524eb37`  
		Last Modified: Wed, 20 Sep 2023 07:43:14 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cefa246a03cf68fb1d80e7cfae3fb57eb3c0ad043888b6de832a9fb031307c`  
		Last Modified: Wed, 20 Sep 2023 07:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa2f305ae9dadbb91140b74ff0b55c21a9321cf1b8ddbf6797413e3eea2d2717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75137204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070412240a079f03f96fd843af860bce55530819d1f0ba73732445aebf47fbb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:21 GMT
ADD file:013dd6e1187d63722cbaddc725f44bc6789ce42a75e2ae86456088763728139c in / 
# Wed, 11 Oct 2023 18:25:21 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:02:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:02:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:02:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Oct 2023 20:02:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:17 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 11 Oct 2023 20:02:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:02:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:02:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:02:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:02:31 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 11 Oct 2023 20:02:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:02:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:02:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:02:31 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:02:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:466d0c81a91b4dea612f4d4bcbd480b8ee299558a2d50e93104c98a012e7975e`  
		Last Modified: Wed, 11 Oct 2023 18:29:47 GMT  
		Size: 26.0 MB (25967816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d44b3c33bdf895337d17dca5816d4d9daa7d71012220aa038a5693b8794941`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b2740e8143dadd14b66ec7c7289c2c5e75e90163dbee383fad72cf89e79f4f`  
		Last Modified: Wed, 11 Oct 2023 20:03:32 GMT  
		Size: 6.6 MB (6577680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137382532f0542c42cb84e1a5fdcdcb13504bda5718de5fd570c130bde44b664`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 1.2 MB (1164827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b9f77d1d946a7812c227419e9b8818b110541b49879ec86db3ef26ed7c735`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 294.4 KB (294432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ab343adf7c8d530cd168cd80fd5c4e3e73e867d42662ca292794ee1df72d4`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf068f9da038bffffb1c037ffb9b8d11cbfdc732021175ad7b1993752cfc8c`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 41.1 MB (41125414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647ebeffa69c30c6848b4175e63fb64a475d837da5d6a060679e6c37ca84c797`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25c026538023e959504082315cb288d3a5b8ce3d356fff25a69f4531485b7`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a581296999493c8ab5392ca9cfc9ba5a679195a9b5942530da12e5e5c92f7c`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eda0dbc05c34a39770619e7b1ad550d04a7649938ab74245dc823b0bdb2cd8d`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.1.2`

```console
$ docker pull couchdb@sha256:7b3dd1a025f8822045e8b1d7d21bb501df86ca69a520c90f1b1689ec9a41735f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `couchdb:3.1.2` - linux; amd64

```console
$ docker pull couchdb@sha256:4b0621c760955c141e004c5aad11436b5e8da28732e6fc82eafb17b0b7563b6c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80075301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8da47e2251aaf06ffd73ae2a545a48d8c5f3555efb6e2ecd45f52bfe0ef7360c`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:25 GMT
ADD file:a280220815a2a1eb37b2adea38333ec2f2d0c15bef81fb925d2fbb5218f0665f in / 
# Wed, 20 Sep 2023 04:56:25 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:41:24 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:41:25 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:41:33 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:37 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 20 Sep 2023 07:41:37 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:41:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:44 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 20 Sep 2023 07:41:45 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:41:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:41:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:41:59 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:41:59 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:59 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:59 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:42:00 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:42:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:9f1ecb66bc03eb034c0c89c673def85a052c432125468c04e9aab84714aca0dd`  
		Last Modified: Wed, 20 Sep 2023 05:01:44 GMT  
		Size: 27.2 MB (27187412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5339bae7194fb6787f979a78e790921ea71a198c722add3f2b014dd06a37b7d`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f33dff033631360b0277f9d704c9a7aa2d427f70315a3adf7ca8788e71f097c7`  
		Last Modified: Wed, 20 Sep 2023 07:43:18 GMT  
		Size: 6.7 MB (6704607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60de85677f42aee612a87ecc31fb26b473f15d20af2e4011d37a716fe889f2`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 1.3 MB (1259896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794235488f03eb10f081f12179fa3fb036d9d52d8a0664b51430318522ba5e40`  
		Last Modified: Wed, 20 Sep 2023 07:43:17 GMT  
		Size: 294.6 KB (294602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc8ad350c4e5f720f913387118e99041e592baeb703b502b75913bab3f5ae0c`  
		Last Modified: Wed, 20 Sep 2023 07:43:16 GMT  
		Size: 273.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4477cceb3e1a45db30b462264e8b6d1b3280de8a5a16b9a835b08b215cfaa80f`  
		Last Modified: Wed, 20 Sep 2023 07:43:19 GMT  
		Size: 44.6 MB (44621774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e960e8b538e8d6d311da0ac721fc3307a89309b3604e58f8f45df11686d97c3`  
		Last Modified: Wed, 20 Sep 2023 07:43:15 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ede81fe511bbc6234d3cd5f3557208a0058f739ad4fec9a189f300f88307219`  
		Last Modified: Wed, 20 Sep 2023 07:43:14 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47e4cc476b00bc9fc56fc7ecc01fab98ff14c8415e5c5e0d81177d13524eb37`  
		Last Modified: Wed, 20 Sep 2023 07:43:14 GMT  
		Size: 2.1 KB (2059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cefa246a03cf68fb1d80e7cfae3fb57eb3c0ad043888b6de832a9fb031307c`  
		Last Modified: Wed, 20 Sep 2023 07:43:14 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.1.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:fa2f305ae9dadbb91140b74ff0b55c21a9321cf1b8ddbf6797413e3eea2d2717
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75137204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2070412240a079f03f96fd843af860bce55530819d1f0ba73732445aebf47fbb`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:21 GMT
ADD file:013dd6e1187d63722cbaddc725f44bc6789ce42a75e2ae86456088763728139c in / 
# Wed, 11 Oct 2023 18:25:21 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:02:00 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:02:01 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:02:07 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:12 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends gosu tini;     rm -rf /var/lib/apt/lists/*;     gosu nobody true;     tini --version
# Wed, 11 Oct 2023 20:02:12 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:02:17 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:02:17 GMT
ENV COUCHDB_VERSION=3.1.2
# Wed, 11 Oct 2023 20:02:18 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:02:30 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~buster     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:02:31 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:02:31 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:02:31 GMT
COPY file:5f96ca1bf2f6f650a65a16c93abec310412df7ca501bf32df2ac20f99b1a0742 in /usr/local/bin 
# Wed, 11 Oct 2023 20:02:31 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:02:31 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:02:31 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:02:31 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:02:32 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:466d0c81a91b4dea612f4d4bcbd480b8ee299558a2d50e93104c98a012e7975e`  
		Last Modified: Wed, 11 Oct 2023 18:29:47 GMT  
		Size: 26.0 MB (25967816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d44b3c33bdf895337d17dca5816d4d9daa7d71012220aa038a5693b8794941`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b2740e8143dadd14b66ec7c7289c2c5e75e90163dbee383fad72cf89e79f4f`  
		Last Modified: Wed, 11 Oct 2023 20:03:32 GMT  
		Size: 6.6 MB (6577680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137382532f0542c42cb84e1a5fdcdcb13504bda5718de5fd570c130bde44b664`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 1.2 MB (1164827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51b9f77d1d946a7812c227419e9b8818b110541b49879ec86db3ef26ed7c735`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 294.4 KB (294432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89ab343adf7c8d530cd168cd80fd5c4e3e73e867d42662ca292794ee1df72d4`  
		Last Modified: Wed, 11 Oct 2023 20:03:31 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdf068f9da038bffffb1c037ffb9b8d11cbfdc732021175ad7b1993752cfc8c`  
		Last Modified: Wed, 11 Oct 2023 20:03:33 GMT  
		Size: 41.1 MB (41125414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647ebeffa69c30c6848b4175e63fb64a475d837da5d6a060679e6c37ca84c797`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 379.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b25c026538023e959504082315cb288d3a5b8ce3d356fff25a69f4531485b7`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a581296999493c8ab5392ca9cfc9ba5a679195a9b5942530da12e5e5c92f7c`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 2.1 KB (2057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eda0dbc05c34a39770619e7b1ad550d04a7649938ab74245dc823b0bdb2cd8d`  
		Last Modified: Wed, 11 Oct 2023 20:03:29 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2`

```console
$ docker pull couchdb@sha256:af2288c800ff4b8b21d51df3a1097ae320b2a72ee6b3637904fcc139f014530a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `couchdb:3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:a0ee8d7d23760de42fca9956e239027167cd30e2fb25f1d63e46abd3804038f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ec457c0a496f4f6ee43b10a18fc6f10259b8e22ace76820bed6e8f6c1ab522`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:40:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:40:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 07:40:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:40:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:04 GMT
ENV COUCHDB_VERSION=3.2.3
# Wed, 20 Sep 2023 07:41:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:41:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:41:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:41:18 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:41:18 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:18 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:41:19 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:41:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d8dff97665ef4ac74b8ba8b6ce7c6dacc5cfd8685014d8ae7c8f7feaf446e`  
		Last Modified: Wed, 20 Sep 2023 07:42:43 GMT  
		Size: 3.4 KB (3403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce890f4609ba4a6fb1db704f669081b13ba9e73efdcf8ab7ff9def4626c87f`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 5.2 MB (5224541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da104612da233e62f2e400c248c0ed004b6bf438d7fcc0dff894e0fb902a6132`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 610.3 KB (610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059880c0330e5a561bf01de9c2237fe79d400edf3e7f03542441fec49507f4`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 294.4 KB (294416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8b94a510d0b2e68d845d543aefe1aa304c33b9666f1d0876dd65bf82d12044`  
		Last Modified: Wed, 20 Sep 2023 07:43:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c562b7d6b7c7fec72ec755c95e8de9b00b6637b8dedcb577a52eb151ad6deb9`  
		Last Modified: Wed, 20 Sep 2023 07:43:06 GMT  
		Size: 52.2 MB (52186653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558124c6ae72ce7a90c5a62c60f6fe8b64b4710ec5fa17b606ba14272d67d73`  
		Last Modified: Wed, 20 Sep 2023 07:43:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4356c40a3470632eaa907064424131d54164f1d42678b069b3dfcbef26f1e0f5`  
		Last Modified: Wed, 20 Sep 2023 07:43:01 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c77e43e7c79f85528ee7366582f9236aee9d6ab14398d405714d6ee6c87a1a`  
		Last Modified: Wed, 20 Sep 2023 07:43:01 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c098461ab1cd0f5e3f36400aacd9b90c9ae381d167e3e69af46041b4dfa440dd`  
		Last Modified: Wed, 20 Sep 2023 07:43:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:960305e9b35826163f173e8b89eab4112410bee3725c3f0773140932dd9f7877
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.2 MB (85205205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:352add31bc606968e9b4695dc003a06de6c7ca3682ea0d3145b972feb8dabfee`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:39:49 GMT
ADD file:7b3c55926db26568f849247e80abdec3cfd6642929a40f0bbee95e4cb176051e in / 
# Wed, 12 Apr 2023 00:39:49 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:33:39 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:33:39 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:33:45 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:33:48 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:33:48 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:33:53 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:34:12 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 12 Apr 2023 01:34:12 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 12 Apr 2023 01:34:24 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 12 Apr 2023 01:34:24 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 12 Apr 2023 01:34:24 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 12 Apr 2023 01:34:24 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 12 Apr 2023 01:34:25 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 01:34:25 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 01:34:25 GMT
VOLUME [/opt/couchdb/data]
# Wed, 12 Apr 2023 01:34:25 GMT
EXPOSE 4369 5984 9100
# Wed, 12 Apr 2023 01:34:25 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:ebc3dc5a2d72427c585c8cda7574a75d96e04b9a37572bd3af0bff905abefbb9`  
		Last Modified: Wed, 12 Apr 2023 00:42:35 GMT  
		Size: 30.1 MB (30063826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f522824805b9b3818de882a514dd5454399e3c21b512a09e64274bf12d18ab4`  
		Last Modified: Wed, 12 Apr 2023 01:35:29 GMT  
		Size: 3.4 KB (3434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdfaf598c101b0427a73a7b5a1edb3b6229985b64794e6d215eb049125bbd25`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 5.2 MB (5209561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc33796685833f0fdacecb6c4f2078915729822d8fb7a21aada1b767c48b377`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 566.3 KB (566295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356323e70f7127294f4bee19c211582a4af79acc6d1f696d70fc94229c84aa52`  
		Last Modified: Wed, 12 Apr 2023 01:35:27 GMT  
		Size: 294.3 KB (294328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9652526d42f149093060de62ac3b39905fb0bfb8457d6148e4314ef71058a153`  
		Last Modified: Wed, 12 Apr 2023 01:35:44 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d95be693dac094ea4fe70ff2bd1f44b66a9ede007474a31cafcb829c361429`  
		Last Modified: Wed, 12 Apr 2023 01:35:47 GMT  
		Size: 49.1 MB (49063995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61eb7f6826c8440901fb275f2b3c5f6be3e97d95482db6770215d5bd31899ed1`  
		Last Modified: Wed, 12 Apr 2023 01:35:42 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d81fa00cdd93053287b1afda2f3cfda4475c6ac6307dc22125a76f843f21415`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 763.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e726b19dd008ea8df7bf3ce90fa1947f685d2f6fdd3caa36e1f3b6e40526d0`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c78146fce98da16e884fde6d22f444849c69c3da90555e336827ceb2b6a039`  
		Last Modified: Wed, 12 Apr 2023 01:35:43 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:90a95123b16f3f08c9e3b862a7e628ead429c8602d5dc110db1b038b5b47db9f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92383985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c0714b286e5789d8b829c846536d1f8a5308d8cf419fa60995af8b91ab3b55`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 12 Apr 2023 00:08:20 GMT
ADD file:63eb52aaff02c15bceabb87a78eb1b36389066ff4774cf8a754160ca7d509816 in / 
# Wed, 12 Apr 2023 00:08:23 GMT
CMD ["bash"]
# Wed, 12 Apr 2023 01:23:31 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 12 Apr 2023 01:23:35 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 12 Apr 2023 01:23:57 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:24:07 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 12 Apr 2023 01:24:08 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 12 Apr 2023 01:24:27 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 12 Apr 2023 01:25:25 GMT
ENV COUCHDB_VERSION=3.2.2-1
# Wed, 12 Apr 2023 01:25:27 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 12 Apr 2023 01:25:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 12 Apr 2023 01:26:02 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 12 Apr 2023 01:26:02 GMT
COPY --chown=couchdb:couchdbfile:f98e48e4254cb3ec4a766f3b9bd3260f16676a310eb0356ee9775c62edb3e8f3 in /opt/couchdb/etc/ 
# Wed, 12 Apr 2023 01:26:03 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 12 Apr 2023 01:26:05 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 12 Apr 2023 01:26:05 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 12 Apr 2023 01:26:06 GMT
VOLUME [/opt/couchdb/data]
# Wed, 12 Apr 2023 01:26:06 GMT
EXPOSE 4369 5984 9100
# Wed, 12 Apr 2023 01:26:07 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:5b41d5ec640939cf684959234ad3b80909268a32bfd520a31c6720a91521c2fa`  
		Last Modified: Wed, 12 Apr 2023 00:13:13 GMT  
		Size: 35.3 MB (35291995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7569dcea363c11bb071b416ea27193dbe62d8a210fa1f829efabb35b46600dae`  
		Last Modified: Wed, 12 Apr 2023 01:26:25 GMT  
		Size: 3.4 KB (3411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a685c575c0e899abc0410edf84715dd5cf4184fcbd447fdbbcac069795eadd05`  
		Last Modified: Wed, 12 Apr 2023 01:26:26 GMT  
		Size: 6.0 MB (6044117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0283a2882808914c7a35f392d4ad2d2921ccf8b8855ab399e2998c22d061f16e`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 662.1 KB (662116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17deb4c48f5c43beee592bed99d27502afe8c8f60cde1cb4bebb7dce00e877c`  
		Last Modified: Wed, 12 Apr 2023 01:26:24 GMT  
		Size: 294.3 KB (294319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb7661a9384c6767a073bc8e86df2ec2c60bef8bad55fac7ab22d7ecffcdb1f1`  
		Last Modified: Wed, 12 Apr 2023 01:26:48 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74733b44093de42db86284861068e909838a6bca4f3ecf0bfd04eb99d5bf8c79`  
		Last Modified: Wed, 12 Apr 2023 01:26:56 GMT  
		Size: 50.1 MB (50084252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c567dbfb6ac3167b1cd2d6532940fd6fb66d9b5b6a1dedf22d61b92a7b4095eb`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf08299e06354b4674e5fabd7e99da65832d26bc98826c051d261e7a03195099`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 765.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5861e0f3152c23eda58111aaac02f82ed4973711f9a55c51cb55ebb9af6220`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b54774512e47b4b9a6dee9f79bf7ec483b3c7c234e949bc4f6c96fb22a3e8237`  
		Last Modified: Wed, 12 Apr 2023 01:26:46 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.2.3`

```console
$ docker pull couchdb@sha256:0918a4b5f7853612908f1151ca0283e52d2fd34f515c4edd0821f1036b3d4462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `couchdb:3.2.3` - linux; amd64

```console
$ docker pull couchdb@sha256:a0ee8d7d23760de42fca9956e239027167cd30e2fb25f1d63e46abd3804038f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.7 MB (89740998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ec457c0a496f4f6ee43b10a18fc6f10259b8e22ace76820bed6e8f6c1ab522`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:40:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:40:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 07:40:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:40:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:41:04 GMT
ENV COUCHDB_VERSION=3.2.3
# Wed, 20 Sep 2023 07:41:04 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:41:17 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:41:18 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:41:18 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:41:18 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:18 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:18 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:18 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:41:19 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:41:19 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d8dff97665ef4ac74b8ba8b6ce7c6dacc5cfd8685014d8ae7c8f7feaf446e`  
		Last Modified: Wed, 20 Sep 2023 07:42:43 GMT  
		Size: 3.4 KB (3403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce890f4609ba4a6fb1db704f669081b13ba9e73efdcf8ab7ff9def4626c87f`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 5.2 MB (5224541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da104612da233e62f2e400c248c0ed004b6bf438d7fcc0dff894e0fb902a6132`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 610.3 KB (610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059880c0330e5a561bf01de9c2237fe79d400edf3e7f03542441fec49507f4`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 294.4 KB (294416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8b94a510d0b2e68d845d543aefe1aa304c33b9666f1d0876dd65bf82d12044`  
		Last Modified: Wed, 20 Sep 2023 07:43:02 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c562b7d6b7c7fec72ec755c95e8de9b00b6637b8dedcb577a52eb151ad6deb9`  
		Last Modified: Wed, 20 Sep 2023 07:43:06 GMT  
		Size: 52.2 MB (52186653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4558124c6ae72ce7a90c5a62c60f6fe8b64b4710ec5fa17b606ba14272d67d73`  
		Last Modified: Wed, 20 Sep 2023 07:43:00 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4356c40a3470632eaa907064424131d54164f1d42678b069b3dfcbef26f1e0f5`  
		Last Modified: Wed, 20 Sep 2023 07:43:01 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c77e43e7c79f85528ee7366582f9236aee9d6ab14398d405714d6ee6c87a1a`  
		Last Modified: Wed, 20 Sep 2023 07:43:01 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c098461ab1cd0f5e3f36400aacd9b90c9ae381d167e3e69af46041b4dfa440dd`  
		Last Modified: Wed, 20 Sep 2023 07:43:00 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3`

```console
$ docker pull couchdb@sha256:2d7c9bacbe4999d427b833a3066a9e785bb72da38e3a3af1e1788d8841f87efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3` - linux; amd64

```console
$ docker pull couchdb@sha256:e4c237b2cbc8dcaf41ac318d04e398be685c1eb6687720250f108bccafe61f1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78991f849f8c06f9274ce87618c10744071db6c4de7f7e1bedca1ac6e624789e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:40:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:40:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 07:40:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:40:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:45 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 07:40:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:40:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:00 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:41:00 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:41:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d8dff97665ef4ac74b8ba8b6ce7c6dacc5cfd8685014d8ae7c8f7feaf446e`  
		Last Modified: Wed, 20 Sep 2023 07:42:43 GMT  
		Size: 3.4 KB (3403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce890f4609ba4a6fb1db704f669081b13ba9e73efdcf8ab7ff9def4626c87f`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 5.2 MB (5224541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da104612da233e62f2e400c248c0ed004b6bf438d7fcc0dff894e0fb902a6132`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 610.3 KB (610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059880c0330e5a561bf01de9c2237fe79d400edf3e7f03542441fec49507f4`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 294.4 KB (294416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1aa965151c59ad7ac1ad873917848dfee3bdb4812dff9dec0ad409eb2604d8`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02984bcb5a695b4453285847308fa479e6c7eee775b2201fa524ddef8f084729`  
		Last Modified: Wed, 20 Sep 2023 07:42:44 GMT  
		Size: 52.7 MB (52685948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41d7eccab181e399d849912c788f6b8276835df0ba0aeaccc58c07517c39ed9`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4034a7db24e022618eff0e254c6dca735a41cf0024fe7f5cb9f005aac47a7b0`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a600c5fcec0d826f6ebea99e6d9d398ec0f65ab75770b1a77da0b3f60cf833`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bd6ec842fabe6e46b865a146d73a63be473c599e6d82af73a63682feca38ae`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b85e8329747a0bbe733b8c3625920b201478af047193fbc943a1c5571238500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88693275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253383c99318d7ad9a6831c541446261470e5f562dcbea09010b2a0a0e3ef53d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:01:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:01:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:01:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 20:01:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:29 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 20:01:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:01:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 20:01:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:01:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:01:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:01:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:01:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419fa3b20618be35a50656b826eb7bfdde4ef2946317c30c5a3768b38aaa8ba0`  
		Last Modified: Wed, 11 Oct 2023 20:03:05 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a80ec2d98f312cdb02ba63d1a882ab37247fb58659ffe8c2700fb74d2a0eea5`  
		Last Modified: Wed, 11 Oct 2023 20:03:04 GMT  
		Size: 5.2 MB (5210867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0fc376ff63452715c9a8a69338dfdf760491280c2e07909a6682afa27d7121`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 567.1 KB (567072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f7a37f661d9c02365eaf3dbe656c3838a0e3370364cbbc1096e5dd70a0c556`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 295.0 KB (295039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3f9f740e76573fa14868cc22c22cff8c24a6de99120e929a99dc13745da54`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a6ba63731db2ab523a856c11b65978f813bc44c0d24954d701204294de119`  
		Last Modified: Wed, 11 Oct 2023 20:03:06 GMT  
		Size: 52.5 MB (52548769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34294d7475990a1c770f8b0c00af4539f2679bd7b16d8299f6576e70a857bed`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa696bb2506cebba21d95ad6e5f7241fad9de808e98357c0061cf006dadde21d`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3bc6d83499278d2ea489a21230ef90bc400cc5e0e287a4d0efa21a67941821`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91b43446d8c1a3e1c5a14fb64012f452471ee6d253d1d9a4fecbe60dbcc3662`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f7bb9c90ca134dbb51470a71db984c40f76ee21040d37a7a83b570686eed9ad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604f3d59348c58a7dfcb181de5a4796da3efed1ac69dfb7811485cce6c53bc79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:11:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 18:11:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 18:11:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:11:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 18:11:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 18:12:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:12:03 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 18:12:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 18:12:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 18:12:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 18:12:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 18:12:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 18:12:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 18:12:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 18:12:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e790e2c9287694cf9652eb7c41d4826d2dd6355c09e0bf59368ce65009d14`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86edb71aa1531785c515ce961dc9adb23fe3cc93985ad5e2726cf09a9b22cdbf`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 6.0 MB (6046190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbee737be9f30885e44eb893e1016c499cea97cc3c25da02f0acbcd2426f5ae2`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 662.9 KB (662896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03258e5c9f472db9db19a9f68f553c696d7ad308c231a1cdea3524d4cd23678f`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 295.1 KB (295078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b635d512183aec2620576e59c565a891c5c1d545d9cce53ab979f8597c55034f`  
		Last Modified: Wed, 11 Oct 2023 18:13:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b905e7ba03087226b54c39e94e6494a0d4b878aba24d0fe83b1dd1ae88edb`  
		Last Modified: Wed, 11 Oct 2023 18:13:36 GMT  
		Size: 53.7 MB (53663080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8107b2ab7e005312a17c61ad4aabba919c479a1976ebc229b6bfc31c71d94fab`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ff9978944af4317513c68ca373b634280fade1b102d2ec40be616116f7158`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388947061f22f9094e8f2119f222e93e980faea84d73328a0d057f22fe026ff4`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e39de32eeee3db27f768655cdb1570e02a2cec7c7e3a87753acc8bf68f4293`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3` - linux; s390x

```console
$ docker pull couchdb@sha256:9f548cfa416c33e911c223dd11709138cabe43e0e5574f11a621a46b6fbf95a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86993125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592ecdc083e910a2759c594277924f9706573e2afb7a81aae1a6badea2a214b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 10:29:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 10:29:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 10:29:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 10:29:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 10:29:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:18 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 10:29:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 10:29:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 10:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 10:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 10:29:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 10:29:39 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 10:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309ebc55f4ef0cc6e5e6ff20c9e9865ff91632cfa7ec0e587ef781f92a575015`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb7d6b9954c9f37886cdb50b5641d3c61a70ee2b6ebfb00f1a62b17c1a9cdf2`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 5.1 MB (5110402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a1f2e24600d89783f110705b3c4da1812b439bfdc97e7fe4ac30a03ff0cd59`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2fc94dec365b1230ce01b2ba97657b0592d9c53524b031f72071a5a8b3502`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04c13697bb058424f77759f7e28422f4211699c6789c0555dc8355c2df1d0b`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f2fb5ff9494e91ccda88ccc3bf6a22cef8aabbac01b5959791452ec5d2abc`  
		Last Modified: Wed, 20 Sep 2023 10:29:55 GMT  
		Size: 51.4 MB (51354753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c87e354d6bb736d51b75fbab317c69a91f5ba5cc90e4b62c46c920c98db62a`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c933d81f71df9060221fd99d82a101ecf0f1c855b16fb3755bcf94962641b6`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7500a42ce1c25636182c530deddd254dd05a5d92eb343414b028e20e1b41476`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5269f1974cdaa958341c635ad403fe18b4c525fa3dceaddd3806106e041b3e2`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:3.3.2`

```console
$ docker pull couchdb@sha256:2d7c9bacbe4999d427b833a3066a9e785bb72da38e3a3af1e1788d8841f87efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:3.3.2` - linux; amd64

```console
$ docker pull couchdb@sha256:e4c237b2cbc8dcaf41ac318d04e398be685c1eb6687720250f108bccafe61f1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78991f849f8c06f9274ce87618c10744071db6c4de7f7e1bedca1ac6e624789e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:40:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:40:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 07:40:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:40:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:45 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 07:40:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:40:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:00 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:41:00 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:41:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d8dff97665ef4ac74b8ba8b6ce7c6dacc5cfd8685014d8ae7c8f7feaf446e`  
		Last Modified: Wed, 20 Sep 2023 07:42:43 GMT  
		Size: 3.4 KB (3403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce890f4609ba4a6fb1db704f669081b13ba9e73efdcf8ab7ff9def4626c87f`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 5.2 MB (5224541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da104612da233e62f2e400c248c0ed004b6bf438d7fcc0dff894e0fb902a6132`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 610.3 KB (610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059880c0330e5a561bf01de9c2237fe79d400edf3e7f03542441fec49507f4`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 294.4 KB (294416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1aa965151c59ad7ac1ad873917848dfee3bdb4812dff9dec0ad409eb2604d8`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02984bcb5a695b4453285847308fa479e6c7eee775b2201fa524ddef8f084729`  
		Last Modified: Wed, 20 Sep 2023 07:42:44 GMT  
		Size: 52.7 MB (52685948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41d7eccab181e399d849912c788f6b8276835df0ba0aeaccc58c07517c39ed9`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4034a7db24e022618eff0e254c6dca735a41cf0024fe7f5cb9f005aac47a7b0`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a600c5fcec0d826f6ebea99e6d9d398ec0f65ab75770b1a77da0b3f60cf833`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bd6ec842fabe6e46b865a146d73a63be473c599e6d82af73a63682feca38ae`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b85e8329747a0bbe733b8c3625920b201478af047193fbc943a1c5571238500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88693275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253383c99318d7ad9a6831c541446261470e5f562dcbea09010b2a0a0e3ef53d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:01:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:01:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:01:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 20:01:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:29 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 20:01:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:01:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 20:01:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:01:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:01:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:01:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:01:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419fa3b20618be35a50656b826eb7bfdde4ef2946317c30c5a3768b38aaa8ba0`  
		Last Modified: Wed, 11 Oct 2023 20:03:05 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a80ec2d98f312cdb02ba63d1a882ab37247fb58659ffe8c2700fb74d2a0eea5`  
		Last Modified: Wed, 11 Oct 2023 20:03:04 GMT  
		Size: 5.2 MB (5210867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0fc376ff63452715c9a8a69338dfdf760491280c2e07909a6682afa27d7121`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 567.1 KB (567072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f7a37f661d9c02365eaf3dbe656c3838a0e3370364cbbc1096e5dd70a0c556`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 295.0 KB (295039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3f9f740e76573fa14868cc22c22cff8c24a6de99120e929a99dc13745da54`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a6ba63731db2ab523a856c11b65978f813bc44c0d24954d701204294de119`  
		Last Modified: Wed, 11 Oct 2023 20:03:06 GMT  
		Size: 52.5 MB (52548769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34294d7475990a1c770f8b0c00af4539f2679bd7b16d8299f6576e70a857bed`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa696bb2506cebba21d95ad6e5f7241fad9de808e98357c0061cf006dadde21d`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3bc6d83499278d2ea489a21230ef90bc400cc5e0e287a4d0efa21a67941821`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91b43446d8c1a3e1c5a14fb64012f452471ee6d253d1d9a4fecbe60dbcc3662`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f7bb9c90ca134dbb51470a71db984c40f76ee21040d37a7a83b570686eed9ad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604f3d59348c58a7dfcb181de5a4796da3efed1ac69dfb7811485cce6c53bc79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:11:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 18:11:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 18:11:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:11:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 18:11:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 18:12:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:12:03 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 18:12:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 18:12:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 18:12:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 18:12:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 18:12:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 18:12:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 18:12:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 18:12:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e790e2c9287694cf9652eb7c41d4826d2dd6355c09e0bf59368ce65009d14`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86edb71aa1531785c515ce961dc9adb23fe3cc93985ad5e2726cf09a9b22cdbf`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 6.0 MB (6046190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbee737be9f30885e44eb893e1016c499cea97cc3c25da02f0acbcd2426f5ae2`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 662.9 KB (662896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03258e5c9f472db9db19a9f68f553c696d7ad308c231a1cdea3524d4cd23678f`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 295.1 KB (295078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b635d512183aec2620576e59c565a891c5c1d545d9cce53ab979f8597c55034f`  
		Last Modified: Wed, 11 Oct 2023 18:13:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b905e7ba03087226b54c39e94e6494a0d4b878aba24d0fe83b1dd1ae88edb`  
		Last Modified: Wed, 11 Oct 2023 18:13:36 GMT  
		Size: 53.7 MB (53663080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8107b2ab7e005312a17c61ad4aabba919c479a1976ebc229b6bfc31c71d94fab`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ff9978944af4317513c68ca373b634280fade1b102d2ec40be616116f7158`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388947061f22f9094e8f2119f222e93e980faea84d73328a0d057f22fe026ff4`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e39de32eeee3db27f768655cdb1570e02a2cec7c7e3a87753acc8bf68f4293`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:3.3.2` - linux; s390x

```console
$ docker pull couchdb@sha256:9f548cfa416c33e911c223dd11709138cabe43e0e5574f11a621a46b6fbf95a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86993125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592ecdc083e910a2759c594277924f9706573e2afb7a81aae1a6badea2a214b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 10:29:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 10:29:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 10:29:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 10:29:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 10:29:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:18 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 10:29:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 10:29:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 10:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 10:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 10:29:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 10:29:39 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 10:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309ebc55f4ef0cc6e5e6ff20c9e9865ff91632cfa7ec0e587ef781f92a575015`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb7d6b9954c9f37886cdb50b5641d3c61a70ee2b6ebfb00f1a62b17c1a9cdf2`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 5.1 MB (5110402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a1f2e24600d89783f110705b3c4da1812b439bfdc97e7fe4ac30a03ff0cd59`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2fc94dec365b1230ce01b2ba97657b0592d9c53524b031f72071a5a8b3502`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04c13697bb058424f77759f7e28422f4211699c6789c0555dc8355c2df1d0b`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f2fb5ff9494e91ccda88ccc3bf6a22cef8aabbac01b5959791452ec5d2abc`  
		Last Modified: Wed, 20 Sep 2023 10:29:55 GMT  
		Size: 51.4 MB (51354753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c87e354d6bb736d51b75fbab317c69a91f5ba5cc90e4b62c46c920c98db62a`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c933d81f71df9060221fd99d82a101ecf0f1c855b16fb3755bcf94962641b6`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7500a42ce1c25636182c530deddd254dd05a5d92eb343414b028e20e1b41476`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5269f1974cdaa958341c635ad403fe18b4c525fa3dceaddd3806106e041b3e2`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `couchdb:latest`

```console
$ docker pull couchdb@sha256:2d7c9bacbe4999d427b833a3066a9e785bb72da38e3a3af1e1788d8841f87efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `couchdb:latest` - linux; amd64

```console
$ docker pull couchdb@sha256:e4c237b2cbc8dcaf41ac318d04e398be685c1eb6687720250f108bccafe61f1d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90240296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78991f849f8c06f9274ce87618c10744071db6c4de7f7e1bedca1ac6e624789e`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:40:29 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 07:40:30 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 07:40:37 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:40 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 07:40:40 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 07:40:45 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 07:40:45 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 07:40:46 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 07:40:58 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 07:40:59 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 07:41:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 07:41:00 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 07:41:00 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 07:41:00 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 07:41:00 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d8dff97665ef4ac74b8ba8b6ce7c6dacc5cfd8685014d8ae7c8f7feaf446e`  
		Last Modified: Wed, 20 Sep 2023 07:42:43 GMT  
		Size: 3.4 KB (3403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cce890f4609ba4a6fb1db704f669081b13ba9e73efdcf8ab7ff9def4626c87f`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 5.2 MB (5224541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da104612da233e62f2e400c248c0ed004b6bf438d7fcc0dff894e0fb902a6132`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 610.3 KB (610273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be059880c0330e5a561bf01de9c2237fe79d400edf3e7f03542441fec49507f4`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 294.4 KB (294416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1aa965151c59ad7ac1ad873917848dfee3bdb4812dff9dec0ad409eb2604d8`  
		Last Modified: Wed, 20 Sep 2023 07:42:41 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02984bcb5a695b4453285847308fa479e6c7eee775b2201fa524ddef8f084729`  
		Last Modified: Wed, 20 Sep 2023 07:42:44 GMT  
		Size: 52.7 MB (52685948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d41d7eccab181e399d849912c788f6b8276835df0ba0aeaccc58c07517c39ed9`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 380.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4034a7db24e022618eff0e254c6dca735a41cf0024fe7f5cb9f005aac47a7b0`  
		Last Modified: Wed, 20 Sep 2023 07:42:39 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a600c5fcec0d826f6ebea99e6d9d398ec0f65ab75770b1a77da0b3f60cf833`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 2.2 KB (2227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bd6ec842fabe6e46b865a146d73a63be473c599e6d82af73a63682feca38ae`  
		Last Modified: Wed, 20 Sep 2023 07:42:38 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; arm64 variant v8

```console
$ docker pull couchdb@sha256:6b85e8329747a0bbe733b8c3625920b201478af047193fbc943a1c5571238500
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88693275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:253383c99318d7ad9a6831c541446261470e5f562dcbea09010b2a0a0e3ef53d`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:06 GMT
ADD file:2c3e5451390c62f0b85f20139d2c88011cc54d649cdda5567084c050ad373372 in / 
# Wed, 11 Oct 2023 18:25:06 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 20:01:15 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 20:01:16 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 20:01:21 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:24 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 20:01:24 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 20:01:29 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 20:01:29 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 20:01:29 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 20:01:41 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 20:01:42 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 20:01:42 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 20:01:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 20:01:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 20:01:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 20:01:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:85e50d2242ceaba78c3726e059dbd2fa06f5c18e265554bd43a482d19b256d20`  
		Last Modified: Wed, 11 Oct 2023 18:29:07 GMT  
		Size: 30.1 MB (30064086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419fa3b20618be35a50656b826eb7bfdde4ef2946317c30c5a3768b38aaa8ba0`  
		Last Modified: Wed, 11 Oct 2023 20:03:05 GMT  
		Size: 3.4 KB (3437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a80ec2d98f312cdb02ba63d1a882ab37247fb58659ffe8c2700fb74d2a0eea5`  
		Last Modified: Wed, 11 Oct 2023 20:03:04 GMT  
		Size: 5.2 MB (5210867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0fc376ff63452715c9a8a69338dfdf760491280c2e07909a6682afa27d7121`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 567.1 KB (567072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58f7a37f661d9c02365eaf3dbe656c3838a0e3370364cbbc1096e5dd70a0c556`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 295.0 KB (295039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf3f9f740e76573fa14868cc22c22cff8c24a6de99120e929a99dc13745da54`  
		Last Modified: Wed, 11 Oct 2023 20:03:03 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25a6ba63731db2ab523a856c11b65978f813bc44c0d24954d701204294de119`  
		Last Modified: Wed, 11 Oct 2023 20:03:06 GMT  
		Size: 52.5 MB (52548769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34294d7475990a1c770f8b0c00af4539f2679bd7b16d8299f6576e70a857bed`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa696bb2506cebba21d95ad6e5f7241fad9de808e98357c0061cf006dadde21d`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 999.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3bc6d83499278d2ea489a21230ef90bc400cc5e0e287a4d0efa21a67941821`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91b43446d8c1a3e1c5a14fb64012f452471ee6d253d1d9a4fecbe60dbcc3662`  
		Last Modified: Wed, 11 Oct 2023 20:03:01 GMT  
		Size: 120.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; ppc64le

```console
$ docker pull couchdb@sha256:f7bb9c90ca134dbb51470a71db984c40f76ee21040d37a7a83b570686eed9ad1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.0 MB (95968380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:604f3d59348c58a7dfcb181de5a4796da3efed1ac69dfb7811485cce6c53bc79`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:53 GMT
ADD file:96450fb62af4cd68105cbbf612cb5d2f79139cc9416835b6c2fdf40727635939 in / 
# Wed, 11 Oct 2023 17:44:55 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:11:13 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 11 Oct 2023 18:11:15 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 11 Oct 2023 18:11:36 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:11:44 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 11 Oct 2023 18:11:45 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 11 Oct 2023 18:12:01 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:12:03 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 11 Oct 2023 18:12:07 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 11 Oct 2023 18:12:37 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 11 Oct 2023 18:12:39 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 11 Oct 2023 18:12:40 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 11 Oct 2023 18:12:41 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 11 Oct 2023 18:12:42 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 11 Oct 2023 18:12:42 GMT
VOLUME [/opt/couchdb/data]
# Wed, 11 Oct 2023 18:12:42 GMT
EXPOSE 4369 5984 9100
# Wed, 11 Oct 2023 18:12:43 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:cde4df93466f96fbb1bbc513d09d354ea1e58d3e619c19fcf9120dbba87405ea`  
		Last Modified: Wed, 11 Oct 2023 17:50:55 GMT  
		Size: 35.3 MB (35293715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175e790e2c9287694cf9652eb7c41d4826d2dd6355c09e0bf59368ce65009d14`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 3.4 KB (3415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86edb71aa1531785c515ce961dc9adb23fe3cc93985ad5e2726cf09a9b22cdbf`  
		Last Modified: Wed, 11 Oct 2023 18:13:32 GMT  
		Size: 6.0 MB (6046190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbee737be9f30885e44eb893e1016c499cea97cc3c25da02f0acbcd2426f5ae2`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 662.9 KB (662896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03258e5c9f472db9db19a9f68f553c696d7ad308c231a1cdea3524d4cd23678f`  
		Last Modified: Wed, 11 Oct 2023 18:13:30 GMT  
		Size: 295.1 KB (295078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b635d512183aec2620576e59c565a891c5c1d545d9cce53ab979f8597c55034f`  
		Last Modified: Wed, 11 Oct 2023 18:13:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7b905e7ba03087226b54c39e94e6494a0d4b878aba24d0fe83b1dd1ae88edb`  
		Last Modified: Wed, 11 Oct 2023 18:13:36 GMT  
		Size: 53.7 MB (53663080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8107b2ab7e005312a17c61ad4aabba919c479a1976ebc229b6bfc31c71d94fab`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 381.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0ff9978944af4317513c68ca373b634280fade1b102d2ec40be616116f7158`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 998.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388947061f22f9094e8f2119f222e93e980faea84d73328a0d057f22fe026ff4`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 2.2 KB (2228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e39de32eeee3db27f768655cdb1570e02a2cec7c7e3a87753acc8bf68f4293`  
		Last Modified: Wed, 11 Oct 2023 18:13:27 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `couchdb:latest` - linux; s390x

```console
$ docker pull couchdb@sha256:9f548cfa416c33e911c223dd11709138cabe43e0e5574f11a621a46b6fbf95a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (86993125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a592ecdc083e910a2759c594277924f9706573e2afb7a81aae1a6badea2a214b`
-	Entrypoint: `["tini","--","\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/couchdb\/bin\/couchdb"]`

```dockerfile
# Wed, 20 Sep 2023 02:54:54 GMT
ADD file:02a97e0d5f41f84ac0284849646284fa41b5e324d24f4d95bb1e2419899da811 in / 
# Wed, 20 Sep 2023 02:54:57 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 10:29:03 GMT
LABEL maintainer=CouchDB Developers dev@couchdb.apache.org
# Wed, 20 Sep 2023 10:29:03 GMT
RUN groupadd -g 5984 -r couchdb && useradd -u 5984 -d /opt/couchdb -g couchdb couchdb
# Wed, 20 Sep 2023 10:29:10 GMT
RUN set -ex;     apt-get update;     apt-get install -y --no-install-recommends         apt-transport-https         ca-certificates         dirmngr         gnupg      ;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:13 GMT
RUN set -eux;     apt-get update;     apt-get install -y --no-install-recommends tini;     rm -rf /var/lib/apt/lists/*;     tini --version
# Wed, 20 Sep 2023 10:29:13 GMT
ENV GPG_COUCH_KEY=390EF70BB1EA12B2773962950EE62FB37A00258D
# Wed, 20 Sep 2023 10:29:18 GMT
RUN set -eux;     apt-get update;     apt-get install -y curl;     export GNUPGHOME="$(mktemp -d)";     curl -fL -o keys.asc https://couchdb.apache.org/repo/keys.asc;     gpg --batch --import keys.asc;     gpg --batch --export "${GPG_COUCH_KEY}" > /usr/share/keyrings/couchdb-archive-keyring.gpg;     command -v gpgconf && gpgconf --kill all || :;     rm -rf "$GNUPGHOME";     apt-key list;     apt purge -y --autoremove curl;     rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 10:29:18 GMT
ENV COUCHDB_VERSION=3.3.2
# Wed, 20 Sep 2023 10:29:19 GMT
RUN . /etc/os-release;     echo "deb [signed-by=/usr/share/keyrings/couchdb-archive-keyring.gpg] https://apache.jfrog.io/artifactory/couchdb-deb/ ${VERSION_CODENAME} main" |         tee /etc/apt/sources.list.d/couchdb.list >/dev/null
# Wed, 20 Sep 2023 10:29:35 GMT
RUN set -eux;     apt-get update;         echo "couchdb couchdb/mode select none" | debconf-set-selections;     DEBIAN_FRONTEND=noninteractive apt-get install -y --allow-downgrades --allow-remove-essential --allow-change-held-packages             couchdb="$COUCHDB_VERSION"~bullseye     ;     rmdir /var/lib/couchdb /var/log/couchdb;     rm /opt/couchdb/data /opt/couchdb/var/log;     mkdir -p /opt/couchdb/data /opt/couchdb/var/log;     chown couchdb:couchdb /opt/couchdb/data /opt/couchdb/var/log;     chmod 777 /opt/couchdb/data /opt/couchdb/var/log;     rm /opt/couchdb/etc/default.d/10-filelog.ini;     find /opt/couchdb \! \( -user couchdb -group couchdb \) -exec chown -f couchdb:couchdb '{}' +;     find /opt/couchdb/etc -type d ! -perm 0755 -exec chmod -f 0755 '{}' +;     find /opt/couchdb/etc -type f ! -perm 0644 -exec chmod -f 0644 '{}' +;     chmod -f 0777 /opt/couchdb/etc/local.d;     rm -rf /var/lib/apt/lists/*;
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:459581cb8ff69dbc1cb246db7b488d5b6127e57fcbb0d0df1288722b5cd25111 in /opt/couchdb/etc/default.d/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY --chown=couchdb:couchdbfile:ef998123ee941cb75b9e8f8c244fd9e244aff7d6394013d8db7515f50882f0cd in /opt/couchdb/etc/ 
# Wed, 20 Sep 2023 10:29:38 GMT
COPY file:cb88dd5d91ff7eac8d8abd6ec372df4f0e05b7787b7d3622916ee9dbe8ea0c85 in /usr/local/bin 
# Wed, 20 Sep 2023 10:29:39 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /docker-entrypoint.sh # backwards compat
# Wed, 20 Sep 2023 10:29:39 GMT
ENTRYPOINT ["tini" "--" "/docker-entrypoint.sh"]
# Wed, 20 Sep 2023 10:29:39 GMT
VOLUME [/opt/couchdb/data]
# Wed, 20 Sep 2023 10:29:39 GMT
EXPOSE 4369 5984 9100
# Wed, 20 Sep 2023 10:29:39 GMT
CMD ["/opt/couchdb/bin/couchdb"]
```

-	Layers:
	-	`sha256:d2d51167e651784cce0bd658d0c2caa328adef8ccf264d8c09860a95bc2a2fc6`  
		Last Modified: Wed, 20 Sep 2023 03:00:22 GMT  
		Size: 29.7 MB (29653129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309ebc55f4ef0cc6e5e6ff20c9e9865ff91632cfa7ec0e587ef781f92a575015`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 3.4 KB (3435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb7d6b9954c9f37886cdb50b5641d3c61a70ee2b6ebfb00f1a62b17c1a9cdf2`  
		Last Modified: Wed, 20 Sep 2023 10:29:52 GMT  
		Size: 5.1 MB (5110402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a1f2e24600d89783f110705b3c4da1812b439bfdc97e7fe4ac30a03ff0cd59`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 573.0 KB (573005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf2fc94dec365b1230ce01b2ba97657b0592d9c53524b031f72071a5a8b3502`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 294.4 KB (294391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf04c13697bb058424f77759f7e28422f4211699c6789c0555dc8355c2df1d0b`  
		Last Modified: Wed, 20 Sep 2023 10:29:51 GMT  
		Size: 275.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5f2fb5ff9494e91ccda88ccc3bf6a22cef8aabbac01b5959791452ec5d2abc`  
		Last Modified: Wed, 20 Sep 2023 10:29:55 GMT  
		Size: 51.4 MB (51354753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c87e354d6bb736d51b75fbab317c69a91f5ba5cc90e4b62c46c920c98db62a`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 382.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40c933d81f71df9060221fd99d82a101ecf0f1c855b16fb3755bcf94962641b6`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 1.0 KB (1003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7500a42ce1c25636182c530deddd254dd05a5d92eb343414b028e20e1b41476`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 2.2 KB (2229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5269f1974cdaa958341c635ad403fe18b4c525fa3dceaddd3806106e041b3e2`  
		Last Modified: Wed, 20 Sep 2023 10:29:50 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
