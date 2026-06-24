## `hylang:1-pypy-bookworm`

```console
$ docker pull hylang@sha256:07c58162198a4960a9dd1a089c1ca769f2c7ad3c9841199dcfcf3bcf4fe1ff16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:6635d999a61c11ec481b3afe3493518f1e5ec7d36060501f0772609d09360f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77238229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad9327f6a022599b01ee84ccb4279d63f55fa982ad52cc4480770867066bfec3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:57:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:57:47 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:57:47 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:57:47 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 01:57:47 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 01:57:47 GMT
CMD ["pypy3"]
# Wed, 24 Jun 2026 02:46:50 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:46:50 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:46:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:46:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3caeebe6bd456c289b2635cfad54d4a086594cb6eb8164ddaef0b9707e872f5a`  
		Last Modified: Wed, 24 Jun 2026 01:57:58 GMT  
		Size: 3.5 MB (3511582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3619d19eae3f7d4487edf8042c0cc8f0c3052ebdfc40c33eb6fb873ecefe08`  
		Last Modified: Wed, 24 Jun 2026 01:58:00 GMT  
		Size: 38.2 MB (38162992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2faf740d7c9a177ef2e30617e1b6e93789b0e65721f59dc8ab3a730aac54b4dc`  
		Last Modified: Wed, 24 Jun 2026 02:46:59 GMT  
		Size: 7.3 MB (7326016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:e806d30942d512447ceaab6f9532d017a9033306dfb6ba3354db90d148fb4038
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddf3b5370dc45b41a7f153ed826d18c8adc8baca854a278425acc843fc4bb973`

```dockerfile
```

-	Layers:
	-	`sha256:f7d1082a2bca8fd2f2ee7006f40f91154ee32534345ccc0539fc21d061a1de59`  
		Last Modified: Wed, 24 Jun 2026 02:46:58 GMT  
		Size: 2.7 MB (2683567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd04218601329efc73ed01fbe30b1fddfaf3d61f75fff6a924c2d95c87735d32`  
		Last Modified: Wed, 24 Jun 2026 02:46:58 GMT  
		Size: 8.9 KB (8899 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:37fd3eab105075c1d9486fb10e9b62fc1dcaacfd4248ef32cbcb98ba9e5a0694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75137847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b65b908c5430ac2cceb96ed69207873d26e44fc607cb1070019b2fca204b6784`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:01:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:14 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:02:14 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:14 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 02:02:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 02:02:14 GMT
CMD ["pypy3"]
# Wed, 24 Jun 2026 02:53:31 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:53:31 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:53:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:53:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8130abcc32f44dd313ce589daa9f6765823514d4ddd83e38994c8c8a1120312`  
		Last Modified: Wed, 24 Jun 2026 02:02:26 GMT  
		Size: 3.3 MB (3344967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6d357872818f7b32c7e69dfe695ba8939fbebd958b98ef1d1b0cffcdc2dc234`  
		Last Modified: Wed, 24 Jun 2026 02:02:27 GMT  
		Size: 36.3 MB (36344417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8abb7a66fbb9f98d54ab668cfb7941c4032be0ae2b81ef803010a90182b2a58`  
		Last Modified: Wed, 24 Jun 2026 02:53:39 GMT  
		Size: 7.3 MB (7326045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:778c7447da445daab133995a14f93c753e9bccffedba78d840adbad0d880238f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4392c8d52827efe49f91f9baedb3cf0df70e6791678541b6413245d77f68c11a`

```dockerfile
```

-	Layers:
	-	`sha256:970dff76034812a2eaa086f00b621ed83423085558c7146ed60800570acfbfe2`  
		Last Modified: Wed, 24 Jun 2026 02:53:39 GMT  
		Size: 2.7 MB (2683886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8618c9c1f9d14564cd348ccc39025635e8d81a9e567be113e3730beafac6a31e`  
		Last Modified: Wed, 24 Jun 2026 02:53:39 GMT  
		Size: 9.1 KB (9051 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:38dabdcc335ffe2aeda7a7f3e156eac3d23580cef1d1c2ac53527a5b66257daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74363083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3f6fae6dd5b36f7309acb188bab8824450d39b26c5898ab7e0324ffb153fca`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:55:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 00:56:12 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 00:56:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 00:56:12 GMT
ENV PYPY_VERSION=7.3.23
# Thu, 11 Jun 2026 00:56:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 11 Jun 2026 00:56:12 GMT
CMD ["pypy3"]
# Thu, 11 Jun 2026 02:40:12 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:40:12 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:40:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:40:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:707460b758530d4476f3fefff30544db7cf8dbd98838ccc3533bc05e79016be4`  
		Last Modified: Wed, 10 Jun 2026 23:40:00 GMT  
		Size: 29.2 MB (29225762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acef1cba6e7922c39277c611a15cec1ac84c2f2f44d96b7c67781751328a7ffc`  
		Last Modified: Thu, 11 Jun 2026 00:56:22 GMT  
		Size: 3.5 MB (3515689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd28a8d53c732f7ffe3bcc8b960dcefa8fe5828eafeda43cacabb8b419ff7d80`  
		Last Modified: Thu, 11 Jun 2026 00:56:23 GMT  
		Size: 34.3 MB (34295594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009146c00ae06dfc3d724d5beda81e8234699613068c9bfe1985ff02620f1cad`  
		Last Modified: Thu, 11 Jun 2026 02:40:20 GMT  
		Size: 7.3 MB (7326038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a47a262a3235e7c021bee4d87ac8bad4bdc45f06378dc7f538f08562aae63a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad1ff067477a472a0433716923edfcd6e079174dcf5d454f2f03d11998032228`

```dockerfile
```

-	Layers:
	-	`sha256:491652001fabd5f959e9958aa95c81040e6ebbd3b1e71f79895fdefb0dda4da2`  
		Last Modified: Thu, 11 Jun 2026 02:40:19 GMT  
		Size: 2.7 MB (2680702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59b7f9113c88b6d3a19e0b858efc40ca89bfeaa84bdb6a6dfdada9f203b83202`  
		Last Modified: Thu, 11 Jun 2026 02:40:19 GMT  
		Size: 8.8 KB (8848 bytes)  
		MIME: application/vnd.in-toto+json
