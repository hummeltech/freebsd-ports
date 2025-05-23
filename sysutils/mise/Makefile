PORTNAME=	mise
DISTVERSIONPREFIX=	v
DISTVERSION=	2025.3.10
CATEGORIES=	sysutils

MAINTAINER=	yuri@FreeBSD.org
COMMENT=	Runtime Executor (asdf rust clone)
WWW=		https://mise.jdx.dev/ \
		https://github.com/jdx/mise

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

BROKEN_armv7=	compilation fails: LLVM ERROR: out of memory

BUILD_DEPENDS=	rust-nightly>0:lang/rust-nightly # because feature `edition2024` is required
LIB_DEPENDS=	libgit2.so:devel/libgit2 \
		libssh2.so:security/libssh2 \
		libzstd.so:archivers/zstd

USES=		cargo localbase:ldflags pkgconfig ssl

USE_GITHUB=	yes
GH_ACCOUNT=	jdx

CARGO_BUILDDEP=	no
CARGO_CRATES=	addr2line-0.21.0 \
		adler-1.0.2 \
		adler2-2.0.0 \
		aead-0.5.2 \
		aes-0.8.4 \
		aes-gcm-0.10.3 \
		age-0.10.1 \
		age-core-0.10.0 \
		ahash-0.8.11 \
		aho-corasick-1.1.3 \
		allocator-api2-0.2.21 \
		android-tzdata-0.1.1 \
		android_system_properties-0.1.5 \
		ansi-str-0.8.0 \
		ansitok-0.2.0 \
		anstream-0.6.18 \
		anstyle-1.0.10 \
		anstyle-parse-0.2.6 \
		anstyle-query-1.1.2 \
		anstyle-wincon-3.0.7 \
		anyhow-1.0.97 \
		arbitrary-1.4.1 \
		arc-swap-1.7.1 \
		arrayvec-0.5.2 \
		arrayvec-0.7.6 \
		assert-json-diff-2.0.2 \
		async-compression-0.4.22 \
		async-trait-0.1.88 \
		atomic-waker-1.1.2 \
		autocfg-1.4.0 \
		backtrace-0.3.71 \
		base64-0.21.7 \
		base64-0.22.1 \
		base64ct-1.7.3 \
		basic-toml-0.1.10 \
		bech32-0.9.1 \
		beef-0.5.2 \
		binstall-tar-0.4.42 \
		bit-set-0.6.0 \
		bit-vec-0.7.0 \
		bitflags-2.9.0 \
		block-buffer-0.10.4 \
		bstr-1.11.3 \
		built-0.7.7 \
		bumpalo-3.17.0 \
		bytecount-0.6.8 \
		byteorder-1.5.0 \
		bytes-1.10.1 \
		bytesize-1.3.2 \
		bzip2-0.5.2 \
		bzip2-sys-0.1.13+1.0.8 \
		calm_io-0.1.1 \
		calmio_filters-0.1.0 \
		cc-1.2.17 \
		cfg-if-1.0.0 \
		cfg_aliases-0.2.1 \
		chacha20-0.9.1 \
		chacha20poly1305-0.10.1 \
		chrono-0.4.40 \
		chrono-tz-0.9.0 \
		chrono-tz-build-0.3.0 \
		ci_info-0.14.14 \
		cipher-0.4.4 \
		clap-4.5.33 \
		clap_builder-4.5.33 \
		clap_derive-4.5.32 \
		clap_lex-0.7.4 \
		clap_mangen-0.2.26 \
		clru-0.6.2 \
		color-eyre-0.6.3 \
		color-print-0.3.7 \
		color-print-proc-macro-0.3.7 \
		color-spantrace-0.2.1 \
		colorchoice-1.0.3 \
		colored-3.0.0 \
		comfy-table-7.1.4 \
		confique-0.3.0 \
		confique-macro-0.0.11 \
		console-0.15.11 \
		const-oid-0.9.6 \
		constant_time_eq-0.3.1 \
		contracts-0.6.3 \
		convert_case-0.4.0 \
		cookie-factory-0.3.3 \
		core-foundation-0.9.4 \
		core-foundation-0.10.0 \
		core-foundation-sys-0.8.7 \
		countme-3.0.1 \
		cpufeatures-0.2.17 \
		crc-3.2.1 \
		crc-catalog-2.4.0 \
		crc32fast-1.4.2 \
		crossbeam-channel-0.5.14 \
		crossbeam-deque-0.8.6 \
		crossbeam-epoch-0.9.18 \
		crossbeam-utils-0.8.21 \
		crossterm-0.28.1 \
		crossterm_winapi-0.9.1 \
		crypto-common-0.1.6 \
		ctor-0.4.1 \
		ctor-proc-macro-0.0.5 \
		ctr-0.9.2 \
		curve25519-dalek-4.1.3 \
		curve25519-dalek-derive-0.1.1 \
		darling-0.20.10 \
		darling_core-0.20.10 \
		darling_macro-0.20.10 \
		dashmap-5.5.3 \
		dashmap-6.1.0 \
		deflate64-0.1.9 \
		demand-1.6.5 \
		der-0.7.9 \
		deranged-0.4.1 \
		derive_arbitrary-1.4.1 \
		derive_more-0.99.19 \
		deunicode-1.6.1 \
		diff-0.1.13 \
		digest-0.10.7 \
		directories-5.0.1 \
		dirs-sys-0.4.1 \
		displaydoc-0.2.5 \
		document-features-0.2.11 \
		dotenvy-0.15.7 \
		dtor-0.0.5 \
		dtor-proc-macro-0.0.5 \
		duct-0.13.7 \
		dunce-1.0.5 \
		ed25519-2.2.3 \
		ed25519-dalek-2.1.1 \
		either-1.15.0 \
		encode_unicode-1.0.0 \
		encoding_rs-0.8.35 \
		env_filter-0.1.3 \
		env_home-0.1.0 \
		env_logger-0.11.7 \
		envmnt-0.10.4 \
		equivalent-1.0.2 \
		erased-serde-0.4.6 \
		errno-0.2.8 \
		errno-0.3.10 \
		errno-dragonfly-0.1.2 \
		exec-0.3.1 \
		expr-lang-0.3.0 \
		eyre-0.6.12 \
		faster-hex-0.9.0 \
		fastrand-2.3.0 \
		fiat-crypto-0.2.9 \
		filetime-0.2.25 \
		filetime_creation-0.2.0 \
		find-crate-0.6.3 \
		fixedbitset-0.5.7 \
		flate2-1.1.0 \
		fluent-0.16.1 \
		fluent-bundle-0.15.3 \
		fluent-langneg-0.13.0 \
		fluent-syntax-0.11.1 \
		fnv-1.0.7 \
		foldhash-0.1.5 \
		foreign-types-0.3.2 \
		foreign-types-shared-0.1.1 \
		form_urlencoded-1.2.1 \
		fsio-0.4.1 \
		fslock-0.2.1 \
		futures-0.3.31 \
		futures-channel-0.3.31 \
		futures-core-0.3.31 \
		futures-executor-0.3.31 \
		futures-io-0.3.31 \
		futures-macro-0.3.31 \
		futures-sink-0.3.31 \
		futures-task-0.3.31 \
		futures-util-0.3.31 \
		fuzzy-matcher-0.3.7 \
		generic-array-0.14.7 \
		getrandom-0.2.15 \
		getrandom-0.3.2 \
		ghash-0.5.1 \
		gimli-0.28.1 \
		gix-0.70.0 \
		gix-actor-0.33.2 \
		gix-archive-0.19.0 \
		gix-attributes-0.24.0 \
		gix-bitmap-0.2.14 \
		gix-chunk-0.4.11 \
		gix-command-0.4.1 \
		gix-commitgraph-0.26.0 \
		gix-config-0.43.0 \
		gix-config-value-0.14.11 \
		gix-credentials-0.27.0 \
		gix-date-0.9.3 \
		gix-diff-0.50.0 \
		gix-dir-0.12.0 \
		gix-discover-0.38.0 \
		gix-features-0.40.0 \
		gix-filter-0.17.0 \
		gix-fs-0.13.0 \
		gix-glob-0.18.0 \
		gix-hash-0.16.0 \
		gix-hashtable-0.7.0 \
		gix-ignore-0.13.0 \
		gix-index-0.38.0 \
		gix-lock-16.0.0 \
		gix-mailmap-0.25.2 \
		gix-negotiate-0.18.0 \
		gix-object-0.47.0 \
		gix-odb-0.67.0 \
		gix-pack-0.57.0 \
		gix-packetline-0.18.3 \
		gix-packetline-blocking-0.18.2 \
		gix-path-0.10.14 \
		gix-pathspec-0.9.0 \
		gix-prompt-0.9.1 \
		gix-protocol-0.48.0 \
		gix-quote-0.4.15 \
		gix-ref-0.50.0 \
		gix-refspec-0.28.0 \
		gix-revision-0.32.0 \
		gix-revwalk-0.18.0 \
		gix-sec-0.10.11 \
		gix-shallow-0.2.0 \
		gix-status-0.17.0 \
		gix-submodule-0.17.0 \
		gix-tempfile-16.0.0 \
		gix-trace-0.1.12 \
		gix-transport-0.45.0 \
		gix-traverse-0.44.0 \
		gix-url-0.29.0 \
		gix-utils-0.1.14 \
		gix-validate-0.9.3 \
		gix-worktree-0.39.0 \
		gix-worktree-state-0.17.0 \
		gix-worktree-stream-0.19.0 \
		glob-0.3.2 \
		globset-0.4.16 \
		globwalk-0.9.1 \
		h2-0.4.8 \
		hashbrown-0.12.3 \
		hashbrown-0.14.5 \
		hashbrown-0.15.2 \
		heck-0.4.1 \
		heck-0.5.0 \
		hermit-abi-0.3.9 \
		hex-0.4.3 \
		hkdf-0.12.4 \
		hmac-0.12.1 \
		home-0.5.11 \
		homedir-0.3.4 \
		http-1.3.1 \
		http-body-1.0.1 \
		http-body-util-0.1.3 \
		httparse-1.10.1 \
		httpdate-1.0.3 \
		human_format-1.1.0 \
		humansize-2.1.3 \
		hyper-1.6.0 \
		hyper-rustls-0.27.5 \
		hyper-tls-0.6.0 \
		hyper-util-0.1.10 \
		i18n-config-0.4.7 \
		i18n-embed-0.14.1 \
		i18n-embed-fl-0.7.0 \
		i18n-embed-impl-0.8.4 \
		iana-time-zone-0.1.62 \
		iana-time-zone-haiku-0.1.2 \
		icu_collections-1.5.0 \
		icu_locid-1.5.0 \
		icu_locid_transform-1.5.0 \
		icu_locid_transform_data-1.5.1 \
		icu_normalizer-1.5.0 \
		icu_normalizer_data-1.5.1 \
		icu_properties-1.5.1 \
		icu_properties_data-1.5.1 \
		icu_provider-1.5.0 \
		icu_provider_macros-1.5.0 \
		ident_case-1.0.1 \
		idna-1.0.3 \
		idna_adapter-1.2.0 \
		ignore-0.4.23 \
		imara-diff-0.1.8 \
		impl-tools-0.10.3 \
		impl-tools-lib-0.11.1 \
		indenter-0.3.3 \
		indexmap-1.9.3 \
		indexmap-2.8.0 \
		indicatif-0.17.11 \
		indoc-2.0.6 \
		inout-0.1.4 \
		insta-1.42.2 \
		intl-memoizer-0.5.2 \
		intl_pluralrules-7.0.2 \
		io-close-0.3.7 \
		io_tee-0.1.1 \
		ipnet-2.11.0 \
		is_terminal_polyfill-1.70.1 \
		itertools-0.10.5 \
		itertools-0.13.0 \
		itertools-0.14.0 \
		itoa-1.0.15 \
		jiff-0.1.29 \
		jiff-0.2.5 \
		jiff-static-0.2.5 \
		jiff-tzdb-0.1.4 \
		jiff-tzdb-platform-0.1.3 \
		jobserver-0.1.32 \
		js-sys-0.3.77 \
		junction-1.2.0 \
		kdl-6.3.4 \
		kstring-2.0.2 \
		lazy-regex-3.4.1 \
		lazy-regex-proc_macros-3.4.1 \
		lazy_static-1.5.0 \
		libc-0.2.171 \
		libm-0.2.11 \
		libredox-0.1.3 \
		linked-hash-map-0.5.6 \
		linux-raw-sys-0.4.15 \
		linux-raw-sys-0.9.3 \
		litemap-0.7.5 \
		litrs-0.4.1 \
		lock_api-0.4.12 \
		lockfree-object-pool-0.1.6 \
		log-0.4.27 \
		logos-0.12.1 \
		logos-derive-0.12.1 \
		lua-src-547.0.0 \
		luajit-src-210.5.12+a4f56a4 \
		lzma-rs-0.3.0 \
		lzma-rust-0.1.7 \
		lzma-sys-0.1.20 \
		matchers-0.1.0 \
		maybe-async-0.2.10 \
		md-5-0.10.6 \
		memchr-2.7.4 \
		memmap2-0.9.5 \
		miette-7.5.0 \
		miette-derive-7.5.0 \
		mime-0.3.17 \
		minimal-lexical-0.2.1 \
		minisign-verify-0.2.3 \
		miniz_oxide-0.7.4 \
		miniz_oxide-0.8.5 \
		mio-1.0.3 \
		mlua-0.10.3 \
		mlua-sys-0.6.7 \
		mlua_derive-0.10.1 \
		mockito-1.7.0 \
		native-tls-0.2.14 \
		nix-0.29.0 \
		nom-7.1.3 \
		nom-8.0.0 \
		nt-time-0.8.1 \
		nu-ansi-term-0.46.0 \
		num-0.4.3 \
		num-bigint-0.4.6 \
		num-complex-0.4.6 \
		num-conv-0.1.0 \
		num-integer-0.1.46 \
		num-iter-0.1.45 \
		num-rational-0.4.2 \
		num-traits-0.2.19 \
		num_cpus-1.16.0 \
		number_prefix-0.4.0 \
		object-0.32.2 \
		once_cell-1.21.1 \
		opaque-debug-0.3.1 \
		openssl-0.10.71 \
		openssl-macros-0.1.1 \
		openssl-probe-0.1.6 \
		openssl-sys-0.9.106 \
		option-ext-0.2.0 \
		ordered-float-2.10.1 \
		os-release-0.1.0 \
		os_pipe-1.2.1 \
		overload-0.1.1 \
		owo-colors-3.5.0 \
		papergrid-0.13.0 \
		parking_lot-0.12.3 \
		parking_lot_core-0.9.10 \
		parse-zoneinfo-0.3.1 \
		paste-1.0.15 \
		path-absolutize-3.1.1 \
		path-dedot-3.1.1 \
		pbkdf2-0.12.2 \
		percent-encoding-2.3.1 \
		pest-2.8.0 \
		pest_derive-2.8.0 \
		pest_generator-2.8.0 \
		pest_meta-2.8.0 \
		petgraph-0.7.1 \
		phf-0.11.3 \
		phf_codegen-0.11.3 \
		phf_generator-0.11.3 \
		phf_shared-0.11.3 \
		pin-project-1.1.10 \
		pin-project-internal-1.1.10 \
		pin-project-lite-0.2.16 \
		pin-utils-0.1.0 \
		pkcs8-0.10.2 \
		pkg-config-0.3.32 \
		platforms-3.5.0 \
		poly1305-0.8.0 \
		polyval-0.6.2 \
		portable-atomic-1.11.0 \
		portable-atomic-util-0.2.4 \
		powerfmt-0.2.0 \
		ppv-lite86-0.2.21 \
		pretty_assertions-1.4.1 \
		proc-macro-error-1.0.4 \
		proc-macro-error-attr-1.0.4 \
		proc-macro-error-attr2-2.0.0 \
		proc-macro-error2-2.0.1 \
		proc-macro2-1.0.94 \
		prodash-29.0.1 \
		quick-xml-0.37.3 \
		quinn-0.11.7 \
		quinn-proto-0.11.10 \
		quinn-udp-0.5.11 \
		quote-1.0.40 \
		r-efi-5.2.0 \
		rand-0.8.5 \
		rand-0.9.0 \
		rand_chacha-0.3.1 \
		rand_chacha-0.9.0 \
		rand_core-0.6.4 \
		rand_core-0.9.3 \
		rayon-1.10.0 \
		rayon-core-1.12.1 \
		redox_syscall-0.5.10 \
		redox_users-0.4.6 \
		regex-1.11.1 \
		regex-automata-0.1.10 \
		regex-automata-0.4.9 \
		regex-syntax-0.6.29 \
		regex-syntax-0.8.5 \
		reqwest-0.12.15 \
		ring-0.17.14 \
		rmp-0.8.14 \
		rmp-serde-1.3.0 \
		roff-0.2.2 \
		rops-0.1.4 \
		rowan-0.15.16 \
		rust-embed-8.6.0 \
		rust-embed-impl-8.6.0 \
		rust-embed-utils-8.6.0 \
		rustc-demangle-0.1.24 \
		rustc-hash-1.1.0 \
		rustc-hash-2.1.1 \
		rustc_version-0.4.1 \
		rustix-0.38.44 \
		rustix-1.0.3 \
		rustls-0.23.25 \
		rustls-native-certs-0.8.1 \
		rustls-pemfile-2.2.0 \
		rustls-pki-types-1.11.0 \
		rustls-webpki-0.103.1 \
		rustversion-1.0.20 \
		ryu-1.0.20 \
		salsa20-0.10.2 \
		same-file-1.0.6 \
		scc-2.3.3 \
		schannel-0.1.27 \
		scopeguard-1.2.0 \
		scrypt-0.11.0 \
		sdd-3.0.8 \
		secrecy-0.8.0 \
		security-framework-2.11.1 \
		security-framework-3.2.0 \
		security-framework-sys-2.14.0 \
		self-replace-1.5.0 \
		self_cell-0.10.3 \
		self_cell-1.1.0 \
		self_update-0.42.0 \
		semver-1.0.26 \
		serde-1.0.219 \
		serde-value-0.7.0 \
		serde_derive-1.0.219 \
		serde_ignored-0.1.11 \
		serde_json-1.0.140 \
		serde_regex-1.1.0 \
		serde_spanned-0.6.8 \
		serde_urlencoded-0.7.1 \
		serde_with-3.12.0 \
		serde_with_macros-3.12.0 \
		serde_yaml-0.9.34+deprecated \
		serial_test-3.2.0 \
		serial_test_derive-3.2.0 \
		sevenz-rust-0.6.1 \
		sha1-0.10.6 \
		sha1_smol-1.0.1 \
		sha2-0.10.8 \
		sharded-slab-0.1.7 \
		shared_child-1.0.1 \
		shell-escape-0.1.5 \
		shell-words-1.1.0 \
		shlex-1.3.0 \
		signal-hook-0.3.17 \
		signal-hook-registry-1.4.2 \
		signature-2.2.0 \
		simd-adler32-0.3.7 \
		similar-2.7.0 \
		siphasher-1.0.1 \
		slab-0.4.9 \
		slug-0.1.6 \
		smallvec-1.14.0 \
		socket2-0.5.8 \
		spki-0.7.3 \
		stable_deref_trait-1.2.0 \
		static_assertions-1.1.0 \
		strsim-0.10.0 \
		strsim-0.11.1 \
		strum-0.26.3 \
		strum-0.27.1 \
		strum_macros-0.26.4 \
		strum_macros-0.27.1 \
		subtle-2.6.1 \
		syn-1.0.109 \
		syn-2.0.100 \
		sync_wrapper-1.0.2 \
		synstructure-0.13.1 \
		sys-info-0.9.1 \
		system-configuration-0.6.1 \
		system-configuration-sys-0.6.0 \
		tabled-0.17.0 \
		tabled_derive-0.9.0 \
		taplo-0.13.2 \
		tar-0.4.44 \
		tempfile-3.19.1 \
		tera-1.20.0 \
		termcolor-1.4.1 \
		terminal_size-0.4.2 \
		test-log-0.2.17 \
		test-log-macros-0.2.17 \
		text-size-1.1.1 \
		thiserror-1.0.69 \
		thiserror-2.0.12 \
		thiserror-impl-1.0.69 \
		thiserror-impl-2.0.12 \
		thread_local-1.1.8 \
		time-0.3.41 \
		time-core-0.1.4 \
		time-macros-0.2.22 \
		tinystr-0.7.6 \
		tinyvec-1.9.0 \
		tinyvec_macros-0.1.1 \
		tokio-1.44.1 \
		tokio-macros-2.5.0 \
		tokio-native-tls-0.3.1 \
		tokio-rustls-0.26.2 \
		tokio-util-0.7.14 \
		toml-0.5.11 \
		toml-0.8.20 \
		toml_datetime-0.6.8 \
		toml_edit-0.22.24 \
		tower-0.5.2 \
		tower-layer-0.3.3 \
		tower-service-0.3.3 \
		tracing-0.1.41 \
		tracing-attributes-0.1.28 \
		tracing-core-0.1.33 \
		tracing-error-0.2.1 \
		tracing-log-0.2.0 \
		tracing-subscriber-0.3.19 \
		try-lock-0.2.5 \
		type-map-0.5.0 \
		typeid-1.0.3 \
		typenum-1.18.0 \
		ubi-0.6.1 \
		ucd-trie-0.1.7 \
		uluru-3.1.0 \
		unic-char-property-0.9.0 \
		unic-char-range-0.9.0 \
		unic-common-0.9.0 \
		unic-langid-0.9.5 \
		unic-langid-impl-0.9.5 \
		unic-segment-0.9.0 \
		unic-ucd-segment-0.9.0 \
		unic-ucd-version-0.9.0 \
		unicode-bom-2.0.3 \
		unicode-ident-1.0.18 \
		unicode-normalization-0.1.24 \
		unicode-segmentation-1.12.0 \
		unicode-width-0.1.14 \
		unicode-width-0.2.0 \
		universal-hash-0.5.1 \
		unsafe-libyaml-0.2.11 \
		untrusted-0.9.0 \
		url-2.5.4 \
		urlencoding-2.1.3 \
		usage-lib-2.0.7 \
		utf16_iter-1.0.5 \
		utf8_iter-1.0.4 \
		utf8parse-0.2.2 \
		valuable-0.1.1 \
		vcpkg-0.2.15 \
		version_check-0.9.5 \
		versions-6.3.2 \
		versions-7.0.0 \
		vfox-1.0.1 \
		vte-0.10.1 \
		vte_generate_state_changes-0.1.2 \
		walkdir-2.5.0 \
		want-0.3.1 \
		wasi-0.11.0+wasi-snapshot-preview1 \
		wasi-0.14.2+wasi-0.2.4 \
		wasm-bindgen-0.2.100 \
		wasm-bindgen-backend-0.2.100 \
		wasm-bindgen-futures-0.4.50 \
		wasm-bindgen-macro-0.2.100 \
		wasm-bindgen-macro-support-0.2.100 \
		wasm-bindgen-shared-0.2.100 \
		web-sys-0.3.77 \
		web-time-1.1.0 \
		webpki-roots-0.26.8 \
		which-7.0.2 \
		widestring-1.2.0 \
		winapi-0.3.9 \
		winapi-i686-pc-windows-gnu-0.4.0 \
		winapi-util-0.1.9 \
		winapi-x86_64-pc-windows-gnu-0.4.0 \
		windows-0.57.0 \
		windows-core-0.52.0 \
		windows-core-0.57.0 \
		windows-implement-0.57.0 \
		windows-interface-0.57.0 \
		windows-link-0.1.1 \
		windows-registry-0.4.0 \
		windows-result-0.1.2 \
		windows-result-0.3.2 \
		windows-strings-0.3.1 \
		windows-sys-0.48.0 \
		windows-sys-0.52.0 \
		windows-sys-0.59.0 \
		windows-targets-0.48.5 \
		windows-targets-0.52.6 \
		windows-targets-0.53.0 \
		windows_aarch64_gnullvm-0.48.5 \
		windows_aarch64_gnullvm-0.52.6 \
		windows_aarch64_gnullvm-0.53.0 \
		windows_aarch64_msvc-0.48.5 \
		windows_aarch64_msvc-0.52.6 \
		windows_aarch64_msvc-0.53.0 \
		windows_i686_gnu-0.48.5 \
		windows_i686_gnu-0.52.6 \
		windows_i686_gnu-0.53.0 \
		windows_i686_gnullvm-0.52.6 \
		windows_i686_gnullvm-0.53.0 \
		windows_i686_msvc-0.48.5 \
		windows_i686_msvc-0.52.6 \
		windows_i686_msvc-0.53.0 \
		windows_x86_64_gnu-0.48.5 \
		windows_x86_64_gnu-0.52.6 \
		windows_x86_64_gnu-0.53.0 \
		windows_x86_64_gnullvm-0.48.5 \
		windows_x86_64_gnullvm-0.52.6 \
		windows_x86_64_gnullvm-0.53.0 \
		windows_x86_64_msvc-0.48.5 \
		windows_x86_64_msvc-0.52.6 \
		windows_x86_64_msvc-0.53.0 \
		winnow-0.6.24 \
		winnow-0.7.4 \
		winsafe-0.0.19 \
		wit-bindgen-rt-0.39.0 \
		write16-1.0.0 \
		writeable-0.5.5 \
		x25519-dalek-2.0.1 \
		xattr-1.5.0 \
		xx-2.0.5 \
		xz2-0.1.7 \
		yansi-1.0.1 \
		yoke-0.7.5 \
		yoke-derive-0.7.5 \
		zerocopy-0.7.35 \
		zerocopy-0.8.24 \
		zerocopy-derive-0.7.35 \
		zerocopy-derive-0.8.24 \
		zerofrom-0.1.6 \
		zerofrom-derive-0.1.6 \
		zeroize-1.8.1 \
		zeroize_derive-1.4.2 \
		zerovec-0.10.4 \
		zerovec-derive-0.10.3 \
		zip-2.5.0 \
		zipsign-api-0.1.3 \
		zopfli-0.8.1 \
		zstd-0.13.3 \
		zstd-safe-7.2.4 \
		zstd-sys-2.0.15+zstd.1.5.7

OPENSSLINC=	/usr/include
OPENSSLLIB=	/usr/lib

PLIST_FILES=	bin/${PORTNAME}

# Fix build on armv7, i386 and powerpc
# sys-info-0.9.1 crate issue: https://github.com/FillZpp/sys-info-rs/issues/80
post-patch:
	@${REINPLACE_CMD} \
	-e '/get_cpu/s|unsigned long|uint64_t|' \
	-e '/get_proc_total/s|unsigned long|uint64_t|' \
	${WRKSRC}/cargo-crates/sys-info-0.9.1/c/*.[ch]

.include <bsd.port.mk>
