<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `mysql`

-	[`mysql:5`](#mysql5)
-	[`mysql:5.6`](#mysql56)
-	[`mysql:5.6.51`](#mysql5651)
-	[`mysql:5.7`](#mysql57)
-	[`mysql:5.7.36`](#mysql5736)
-	[`mysql:8`](#mysql8)
-	[`mysql:8.0`](#mysql80)
-	[`mysql:8.0.27`](#mysql8027)
-	[`mysql:latest`](#mysqllatest)

## `mysql:5`

```console
$ docker pull mysql@sha256:2db8bfd2656b51ded5d938abcded8d32ec6181a9eae8dfc7ddf87a656ef97e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5` - linux; amd64

```console
$ docker pull mysql@sha256:e5f84e8def65d7bd1e5aaf79d429b748d56c514f6dc4b6247fc67df1f7da7a2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154834409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b57d64674c4a123bf8bed384e5e057be77db934303b3023d9be331398b761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:38 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 18 Oct 2021 21:36:06 GMT
ENV MYSQL_VERSION=5.7.36-1debian10
# Mon, 18 Oct 2021 21:36:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:36:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:36:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:36:27 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:28 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71aacf913e7f1eeff8d7aa759f355f8f82b649c7dab34d8622dfb086bbef660`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393153c555df67a5ef986bb36bbb8dfde0d93027cebfb1bf3f26030c93db478f`  
		Last Modified: Mon, 18 Oct 2021 21:37:33 GMT  
		Size: 108.6 MB (108637868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06628e2290d7188f3b8453b211ec2b51e2b04a0312618e4f06eb43ec6a54d5a4`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2ab8dac9ac40ee459dfd8f4d7b5e733d364d654d9b491f7017ab95e41f2be1`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6`

```console
$ docker pull mysql@sha256:cdb7b3a69c0f36ce61dda653cdbe1bf086b6a98c1bf6fa023f7a37bc8325dc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6` - linux; amd64

```console
$ docker pull mysql@sha256:6ba9428c3fbac40577e86367043c044f1edad9738629300ba0602d05bd1b12d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102970747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b364958c233566bff03ad2a44a417c7efe192a08a0ceebbb9b75316ca831d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:24:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:24:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:24:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:24:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:24:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:24:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:24:41 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:24:41 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 12 Oct 2021 16:24:42 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Tue, 12 Oct 2021 16:24:42 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Oct 2021 16:24:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Oct 2021 16:24:58 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Oct 2021 16:24:58 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:24:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 16:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:25:00 GMT
EXPOSE 3306
# Tue, 12 Oct 2021 16:25:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f71fe48852c9b99183aa3fb3e2b06a3f7ed3be6a80daa334d50d699967569b`  
		Last Modified: Tue, 12 Oct 2021 16:26:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bdbff3130a5d3a456985fa0aa55dff7e2fa29ef25cb4a27d02fb2576a4f655`  
		Last Modified: Tue, 12 Oct 2021 16:26:27 GMT  
		Size: 4.5 MB (4503783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b14d18e3a15974a3fb11ed8cfbc1581b366778c499fec9b942cb527d8f04a5`  
		Last Modified: Tue, 12 Oct 2021 16:26:26 GMT  
		Size: 1.4 MB (1412168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ba66db8ef39763b31bb58f3a00350ecb0ce1bb2576b8a3b5a66d519fd97806`  
		Last Modified: Tue, 12 Oct 2021 16:26:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7e25beebfaaab4021d84aa09b67939daa38760fd93fe201332e1e0bd94809`  
		Last Modified: Tue, 12 Oct 2021 16:26:28 GMT  
		Size: 10.2 MB (10225752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d69efd6c310472dc45954a35daea0d44580e6f56a9a0d7c91008f0496d98e27`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 19.5 KB (19458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef665230f46f036e65cac1d260bb2b46a2d1e12a16733d0823f210ee42fbc99c`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f26c5841884ece34d2701091a7188d2a21b63f62d41c4dd39a165a71551e345`  
		Last Modified: Tue, 12 Oct 2021 16:26:34 GMT  
		Size: 64.3 MB (64274226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57157e768b6b8cfc4aaf8579aa43a1f3239fca95eee1361b7224d4d4190f31`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 5.6 KB (5559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b60bbc78c93ed4a3eb1d513c8ff2d592e66ce1e27f2faf233ff3a3a90155c`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.6.51`

```console
$ docker pull mysql@sha256:cdb7b3a69c0f36ce61dda653cdbe1bf086b6a98c1bf6fa023f7a37bc8325dc98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.6.51` - linux; amd64

```console
$ docker pull mysql@sha256:6ba9428c3fbac40577e86367043c044f1edad9738629300ba0602d05bd1b12d1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.0 MB (102970747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b364958c233566bff03ad2a44a417c7efe192a08a0ceebbb9b75316ca831d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:24:07 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:24:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:24:13 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:24:25 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:24:26 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:24:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:24:41 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:24:41 GMT
ENV MYSQL_MAJOR=5.6
# Tue, 12 Oct 2021 16:24:42 GMT
ENV MYSQL_VERSION=5.6.51-1debian9
# Tue, 12 Oct 2021 16:24:42 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ stretch mysql-5.6' > /etc/apt/sources.list.d/mysql.list
# Tue, 12 Oct 2021 16:24:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Tue, 12 Oct 2021 16:24:58 GMT
VOLUME [/var/lib/mysql]
# Tue, 12 Oct 2021 16:24:58 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Tue, 12 Oct 2021 16:24:59 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Tue, 12 Oct 2021 16:24:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Oct 2021 16:25:00 GMT
EXPOSE 3306
# Tue, 12 Oct 2021 16:25:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f71fe48852c9b99183aa3fb3e2b06a3f7ed3be6a80daa334d50d699967569b`  
		Last Modified: Tue, 12 Oct 2021 16:26:28 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bdbff3130a5d3a456985fa0aa55dff7e2fa29ef25cb4a27d02fb2576a4f655`  
		Last Modified: Tue, 12 Oct 2021 16:26:27 GMT  
		Size: 4.5 MB (4503783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b14d18e3a15974a3fb11ed8cfbc1581b366778c499fec9b942cb527d8f04a5`  
		Last Modified: Tue, 12 Oct 2021 16:26:26 GMT  
		Size: 1.4 MB (1412168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45ba66db8ef39763b31bb58f3a00350ecb0ce1bb2576b8a3b5a66d519fd97806`  
		Last Modified: Tue, 12 Oct 2021 16:26:25 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c7e25beebfaaab4021d84aa09b67939daa38760fd93fe201332e1e0bd94809`  
		Last Modified: Tue, 12 Oct 2021 16:26:28 GMT  
		Size: 10.2 MB (10225752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d69efd6c310472dc45954a35daea0d44580e6f56a9a0d7c91008f0496d98e27`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 19.5 KB (19458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef665230f46f036e65cac1d260bb2b46a2d1e12a16733d0823f210ee42fbc99c`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f26c5841884ece34d2701091a7188d2a21b63f62d41c4dd39a165a71551e345`  
		Last Modified: Tue, 12 Oct 2021 16:26:34 GMT  
		Size: 64.3 MB (64274226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc57157e768b6b8cfc4aaf8579aa43a1f3239fca95eee1361b7224d4d4190f31`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 5.6 KB (5559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:934b60bbc78c93ed4a3eb1d513c8ff2d592e66ce1e27f2faf233ff3a3a90155c`  
		Last Modified: Tue, 12 Oct 2021 16:26:23 GMT  
		Size: 117.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7`

```console
$ docker pull mysql@sha256:2db8bfd2656b51ded5d938abcded8d32ec6181a9eae8dfc7ddf87a656ef97e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7` - linux; amd64

```console
$ docker pull mysql@sha256:e5f84e8def65d7bd1e5aaf79d429b748d56c514f6dc4b6247fc67df1f7da7a2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154834409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b57d64674c4a123bf8bed384e5e057be77db934303b3023d9be331398b761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:38 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 18 Oct 2021 21:36:06 GMT
ENV MYSQL_VERSION=5.7.36-1debian10
# Mon, 18 Oct 2021 21:36:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:36:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:36:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:36:27 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:28 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71aacf913e7f1eeff8d7aa759f355f8f82b649c7dab34d8622dfb086bbef660`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393153c555df67a5ef986bb36bbb8dfde0d93027cebfb1bf3f26030c93db478f`  
		Last Modified: Mon, 18 Oct 2021 21:37:33 GMT  
		Size: 108.6 MB (108637868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06628e2290d7188f3b8453b211ec2b51e2b04a0312618e4f06eb43ec6a54d5a4`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2ab8dac9ac40ee459dfd8f4d7b5e733d364d654d9b491f7017ab95e41f2be1`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:5.7.36`

```console
$ docker pull mysql@sha256:2db8bfd2656b51ded5d938abcded8d32ec6181a9eae8dfc7ddf87a656ef97e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:5.7.36` - linux; amd64

```console
$ docker pull mysql@sha256:e5f84e8def65d7bd1e5aaf79d429b748d56c514f6dc4b6247fc67df1f7da7a2c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154834409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:938b57d64674c4a123bf8bed384e5e057be77db934303b3023d9be331398b761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:38 GMT
ENV MYSQL_MAJOR=5.7
# Mon, 18 Oct 2021 21:36:06 GMT
ENV MYSQL_VERSION=5.7.36-1debian10
# Mon, 18 Oct 2021 21:36:06 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-5.7' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:36:26 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-server="${MYSQL_VERSION}" 	&& find /etc/mysql/ -name '*.cnf' -print0 		| xargs -0 grep -lZE '^(bind-address|log)' 		| xargs -rt -0 sed -Ei 's/^(bind-address|log)/#&/' 	&& echo '[mysqld]\nskip-host-cache\nskip-name-resolve' > /etc/mysql/conf.d/docker.cnf 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:36:27 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:36:27 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:28 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:28 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:28 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a71aacf913e7f1eeff8d7aa759f355f8f82b649c7dab34d8622dfb086bbef660`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393153c555df67a5ef986bb36bbb8dfde0d93027cebfb1bf3f26030c93db478f`  
		Last Modified: Mon, 18 Oct 2021 21:37:33 GMT  
		Size: 108.6 MB (108637868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06628e2290d7188f3b8453b211ec2b51e2b04a0312618e4f06eb43ec6a54d5a4`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff2ab8dac9ac40ee459dfd8f4d7b5e733d364d654d9b491f7017ab95e41f2be1`  
		Last Modified: Mon, 18 Oct 2021 21:37:19 GMT  
		Size: 121.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8`

```console
$ docker pull mysql@sha256:6d7d4524463fe6e2b893ffc2b89543c81dec7ef82fb2020a1b27606666464d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8` - linux; amd64

```console
$ docker pull mysql@sha256:975b3b1a6df6bf66221d1702b76c4141a4cd09f93f22f70c32edc99a6c256fe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151432077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac195d15afac2335de52fd7a0e34202fe582731963d31830f1b97700bf9509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:15 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Oct 2021 21:35:42 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Mon, 18 Oct 2021 21:35:43 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:35:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:35:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:35:59 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 18 Oct 2021 21:35:59 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:00 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7421c8152e1c89fb1c1fe3f69d7854dbb6cddfcfb88de18ebb09ac841ca5e4`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f3d8811a286671d5fc412fce8204b7994afd7d6c8d1253dc0852bf240a4772`  
		Last Modified: Mon, 18 Oct 2021 21:37:03 GMT  
		Size: 105.2 MB (105234694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce755338cba16f07595faad71c84feba2b7b5597675f3352c3bc18330fd98e2`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b753046b9f95a7ada2bf95ef5b5f9d493cb4f1cdf6430bd982c54cdec1656f`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e64b0ab53c4d83341c1e8b26b2d9a5b3d4df3c338e4ec6aae98d6cf4c8a65c`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0`

```console
$ docker pull mysql@sha256:6d7d4524463fe6e2b893ffc2b89543c81dec7ef82fb2020a1b27606666464d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0` - linux; amd64

```console
$ docker pull mysql@sha256:975b3b1a6df6bf66221d1702b76c4141a4cd09f93f22f70c32edc99a6c256fe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151432077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac195d15afac2335de52fd7a0e34202fe582731963d31830f1b97700bf9509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:15 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Oct 2021 21:35:42 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Mon, 18 Oct 2021 21:35:43 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:35:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:35:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:35:59 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 18 Oct 2021 21:35:59 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:00 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7421c8152e1c89fb1c1fe3f69d7854dbb6cddfcfb88de18ebb09ac841ca5e4`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f3d8811a286671d5fc412fce8204b7994afd7d6c8d1253dc0852bf240a4772`  
		Last Modified: Mon, 18 Oct 2021 21:37:03 GMT  
		Size: 105.2 MB (105234694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce755338cba16f07595faad71c84feba2b7b5597675f3352c3bc18330fd98e2`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b753046b9f95a7ada2bf95ef5b5f9d493cb4f1cdf6430bd982c54cdec1656f`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e64b0ab53c4d83341c1e8b26b2d9a5b3d4df3c338e4ec6aae98d6cf4c8a65c`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:8.0.27`

```console
$ docker pull mysql@sha256:6d7d4524463fe6e2b893ffc2b89543c81dec7ef82fb2020a1b27606666464d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:8.0.27` - linux; amd64

```console
$ docker pull mysql@sha256:975b3b1a6df6bf66221d1702b76c4141a4cd09f93f22f70c32edc99a6c256fe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151432077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac195d15afac2335de52fd7a0e34202fe582731963d31830f1b97700bf9509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:15 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Oct 2021 21:35:42 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Mon, 18 Oct 2021 21:35:43 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:35:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:35:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:35:59 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 18 Oct 2021 21:35:59 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:00 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7421c8152e1c89fb1c1fe3f69d7854dbb6cddfcfb88de18ebb09ac841ca5e4`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f3d8811a286671d5fc412fce8204b7994afd7d6c8d1253dc0852bf240a4772`  
		Last Modified: Mon, 18 Oct 2021 21:37:03 GMT  
		Size: 105.2 MB (105234694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce755338cba16f07595faad71c84feba2b7b5597675f3352c3bc18330fd98e2`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b753046b9f95a7ada2bf95ef5b5f9d493cb4f1cdf6430bd982c54cdec1656f`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e64b0ab53c4d83341c1e8b26b2d9a5b3d4df3c338e4ec6aae98d6cf4c8a65c`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `mysql:latest`

```console
$ docker pull mysql@sha256:6d7d4524463fe6e2b893ffc2b89543c81dec7ef82fb2020a1b27606666464d87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `mysql:latest` - linux; amd64

```console
$ docker pull mysql@sha256:975b3b1a6df6bf66221d1702b76c4141a4cd09f93f22f70c32edc99a6c256fe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.4 MB (151432077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac195d15afac2335de52fd7a0e34202fe582731963d31830f1b97700bf9509`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["mysqld"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:22:41 GMT
RUN groupadd -r mysql && useradd -r -g mysql mysql
# Tue, 12 Oct 2021 16:22:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends gnupg dirmngr && rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:22:48 GMT
ENV GOSU_VERSION=1.12
# Tue, 12 Oct 2021 16:22:57 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates wget; 	rm -rf /var/lib/apt/lists/*; 	dpkgArch="$(dpkg --print-architecture | awk -F- '{ print $NF }')"; 	wget -O /usr/local/bin/gosu "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch"; 	wget -O /usr/local/bin/gosu.asc "https://github.com/tianon/gosu/releases/download/$GOSU_VERSION/gosu-$dpkgArch.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4; 	gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /usr/local/bin/gosu.asc; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	chmod +x /usr/local/bin/gosu; 	gosu --version; 	gosu nobody true
# Tue, 12 Oct 2021 16:22:58 GMT
RUN mkdir /docker-entrypoint-initdb.d
# Tue, 12 Oct 2021 16:23:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		pwgen 		openssl 		perl 		xz-utils 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:23:15 GMT
RUN set -ex; 	key='A4A9406876FCBD3C456770C88C718D3B5072E1F5'; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	gpg --batch --export "$key" > /etc/apt/trusted.gpg.d/mysql.gpg; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 	apt-key list > /dev/null
# Tue, 12 Oct 2021 16:23:15 GMT
ENV MYSQL_MAJOR=8.0
# Mon, 18 Oct 2021 21:35:42 GMT
ENV MYSQL_VERSION=8.0.27-1debian10
# Mon, 18 Oct 2021 21:35:43 GMT
RUN echo 'deb http://repo.mysql.com/apt/debian/ buster mysql-8.0' > /etc/apt/sources.list.d/mysql.list
# Mon, 18 Oct 2021 21:35:58 GMT
RUN { 		echo mysql-community-server mysql-community-server/data-dir select ''; 		echo mysql-community-server mysql-community-server/root-pass password ''; 		echo mysql-community-server mysql-community-server/re-root-pass password ''; 		echo mysql-community-server mysql-community-server/remove-test-db select false; 	} | debconf-set-selections 	&& apt-get update 	&& apt-get install -y 		mysql-community-client="${MYSQL_VERSION}" 		mysql-community-server-core="${MYSQL_VERSION}" 	&& rm -rf /var/lib/apt/lists/* 	&& rm -rf /var/lib/mysql && mkdir -p /var/lib/mysql /var/run/mysqld 	&& chown -R mysql:mysql /var/lib/mysql /var/run/mysqld 	&& chmod 1777 /var/run/mysqld /var/lib/mysql
# Mon, 18 Oct 2021 21:35:58 GMT
VOLUME [/var/lib/mysql]
# Mon, 18 Oct 2021 21:35:59 GMT
COPY dir:2e040acc386ebd23b8571951a51e6cb93647df091bc26159b8c757ef82b3fcda in /etc/mysql/ 
# Mon, 18 Oct 2021 21:35:59 GMT
COPY file:345a22fe55d3e6783a17075612415413487e7dba27fbf1000a67c7870364b739 in /usr/local/bin/ 
# Mon, 18 Oct 2021 21:36:00 GMT
RUN ln -s usr/local/bin/docker-entrypoint.sh /entrypoint.sh # backwards compat
# Mon, 18 Oct 2021 21:36:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 18 Oct 2021 21:36:00 GMT
EXPOSE 3306 33060
# Mon, 18 Oct 2021 21:36:00 GMT
CMD ["mysqld"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f23cbf2ecc5d6ad68efaf326f8ff1c8b4adfab8faad61315440d21c396dd0160`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cfc6c29c0af103c07adaa5e3ee70ffbd8de71ca7b9155079c9769f45fb9aa4`  
		Last Modified: Tue, 12 Oct 2021 16:25:22 GMT  
		Size: 4.2 MB (4179263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38609286cbe5e62cb8a5a9cb7ed553050e6fc1fa4c537b46c54b6d81a527a7b`  
		Last Modified: Tue, 12 Oct 2021 16:25:20 GMT  
		Size: 1.4 MB (1419434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8211d9e66cd658ab45002b3fa5f8558cd8c13d2f07ba492d7ea1520718d32cff`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2313f9eeca4a60533540741b85137033831959ae5a9c4ea652fa4605c9a14bae`  
		Last Modified: Tue, 12 Oct 2021 16:25:23 GMT  
		Size: 13.4 MB (13448689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eb487d00da0bfa9e36634d8c6ceae1e2116f2b56da6b272bec5233966f989e8`  
		Last Modified: Tue, 12 Oct 2021 16:25:19 GMT  
		Size: 1.9 KB (1879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7421c8152e1c89fb1c1fe3f69d7854dbb6cddfcfb88de18ebb09ac841ca5e4`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f3d8811a286671d5fc412fce8204b7994afd7d6c8d1253dc0852bf240a4772`  
		Last Modified: Mon, 18 Oct 2021 21:37:03 GMT  
		Size: 105.2 MB (105234694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cce755338cba16f07595faad71c84feba2b7b5597675f3352c3bc18330fd98e2`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 842.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b753046b9f95a7ada2bf95ef5b5f9d493cb4f1cdf6430bd982c54cdec1656f`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 5.5 KB (5542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e64b0ab53c4d83341c1e8b26b2d9a5b3d4df3c338e4ec6aae98d6cf4c8a65c`  
		Last Modified: Mon, 18 Oct 2021 21:36:47 GMT  
		Size: 119.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
