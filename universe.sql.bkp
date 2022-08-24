--
-- PostgreSQL database dump
--

-- Dumped from database version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)
-- Dumped by pg_dump version 12.9 (Ubuntu 12.9-2.pgdg20.04+1)

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

DROP DATABASE universe;
--
-- Name: universe; Type: DATABASE; Schema: -; Owner: freecodecamp
--

CREATE DATABASE universe WITH TEMPLATE = template0 ENCODING = 'UTF8' LC_COLLATE = 'C.UTF-8' LC_CTYPE = 'C.UTF-8';


ALTER DATABASE universe OWNER TO freecodecamp;

\connect universe

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- Name: constellation; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.constellation (
    constellation_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text
);


ALTER TABLE public.constellation OWNER TO freecodecamp;

--
-- Name: constellation_constellation_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.constellation_constellation_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.constellation_constellation_id_seq OWNER TO freecodecamp;

--
-- Name: constellation_constellation_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.constellation_constellation_id_seq OWNED BY public.constellation.constellation_id;


--
-- Name: galaxy; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy (
    galaxy_id integer NOT NULL,
    name character varying(30) NOT NULL,
    galaxy_alias character varying(20),
    galaxy_diameter_in_light_years integer NOT NULL,
    galaxy_distance_from_earth_in_million_light_years numeric(7,2)
);


ALTER TABLE public.galaxy OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_galaxy_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_galaxy_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_galaxy_id_seq OWNED BY public.galaxy.galaxy_id;


--
-- Name: galaxy_type; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.galaxy_type (
    galaxy_type_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text
);


ALTER TABLE public.galaxy_type OWNER TO freecodecamp;

--
-- Name: galaxy_type_galaxy_type_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.galaxy_type_galaxy_type_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.galaxy_type_galaxy_type_id_seq OWNER TO freecodecamp;

--
-- Name: galaxy_type_galaxy_type_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.galaxy_type_galaxy_type_id_seq OWNED BY public.galaxy_type.galaxy_type_id;


--
-- Name: moon; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.moon (
    moon_id integer NOT NULL,
    name character varying(30) NOT NULL,
    mean_radius_in_km numeric(6,1) NOT NULL,
    discovery_year integer NOT NULL,
    planet_id integer
);


ALTER TABLE public.moon OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.moon_moon_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.moon_moon_id_seq OWNER TO freecodecamp;

--
-- Name: moon_moon_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.moon_moon_id_seq OWNED BY public.moon.moon_id;


--
-- Name: planet; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet (
    planet_id integer NOT NULL,
    name character varying(30) NOT NULL,
    planet_diameter_in_km numeric(8,1) NOT NULL,
    planet_mass_in_quadrillion_kg bigint NOT NULL,
    number_of_satellite integer NOT NULL,
    has_life boolean,
    is_spherical boolean,
    star_id integer
);


ALTER TABLE public.planet OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_planet_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_planet_id_seq OWNER TO freecodecamp;

--
-- Name: planet_planet_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_planet_id_seq OWNED BY public.planet.planet_id;


--
-- Name: planet_type; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.planet_type (
    planet_type_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text
);


ALTER TABLE public.planet_type OWNER TO freecodecamp;

--
-- Name: planet_type_planet_type_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.planet_type_planet_type_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.planet_type_planet_type_id_seq OWNER TO freecodecamp;

--
-- Name: planet_type_planet_type_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.planet_type_planet_type_id_seq OWNED BY public.planet_type.planet_type_id;


--
-- Name: star; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star (
    star_id integer NOT NULL,
    name character varying(30) NOT NULL,
    star_distance_from_earth_in_light_years numeric(11,7) NOT NULL,
    star_age_in_billion_years numeric(7,2) NOT NULL,
    star_surface_temperature_in_kelvin integer NOT NULL,
    galaxy_id integer
);


ALTER TABLE public.star OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_star_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_star_id_seq OWNER TO freecodecamp;

--
-- Name: star_star_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_star_id_seq OWNED BY public.star.star_id;


--
-- Name: star_type; Type: TABLE; Schema: public; Owner: freecodecamp
--

CREATE TABLE public.star_type (
    star_type_id integer NOT NULL,
    name character varying(30) NOT NULL,
    description text
);


ALTER TABLE public.star_type OWNER TO freecodecamp;

--
-- Name: star_type_star_type_id_seq; Type: SEQUENCE; Schema: public; Owner: freecodecamp
--

CREATE SEQUENCE public.star_type_star_type_id_seq
    AS integer
    START WITH 1
    INCREMENT BY 1
    NO MINVALUE
    NO MAXVALUE
    CACHE 1;


ALTER TABLE public.star_type_star_type_id_seq OWNER TO freecodecamp;

--
-- Name: star_type_star_type_id_seq; Type: SEQUENCE OWNED BY; Schema: public; Owner: freecodecamp
--

ALTER SEQUENCE public.star_type_star_type_id_seq OWNED BY public.star_type.star_type_id;


--
-- Name: constellation constellation_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.constellation ALTER COLUMN constellation_id SET DEFAULT nextval('public.constellation_constellation_id_seq'::regclass);


--
-- Name: galaxy galaxy_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy ALTER COLUMN galaxy_id SET DEFAULT nextval('public.galaxy_galaxy_id_seq'::regclass);


--
-- Name: galaxy_type galaxy_type_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy_type ALTER COLUMN galaxy_type_id SET DEFAULT nextval('public.galaxy_type_galaxy_type_id_seq'::regclass);


--
-- Name: moon moon_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon ALTER COLUMN moon_id SET DEFAULT nextval('public.moon_moon_id_seq'::regclass);


--
-- Name: planet planet_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet ALTER COLUMN planet_id SET DEFAULT nextval('public.planet_planet_id_seq'::regclass);


--
-- Name: planet_type planet_type_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_type ALTER COLUMN planet_type_id SET DEFAULT nextval('public.planet_type_planet_type_id_seq'::regclass);


--
-- Name: star star_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star ALTER COLUMN star_id SET DEFAULT nextval('public.star_star_id_seq'::regclass);


--
-- Name: star_type star_type_id; Type: DEFAULT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star_type ALTER COLUMN star_type_id SET DEFAULT nextval('public.star_type_star_type_id_seq'::regclass);


--
-- Data for Name: constellation; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.constellation VALUES (1, 'Sagittarius', 'It is one of the constellations of the zodiac and is located in the Southern celetial hemisphere. It is one of the 48 constellations listed by the second-century astronomer Ptolemy.');
INSERT INTO public.constellation VALUES (2, 'Virgo', 'Virgo is the second-largest constellation in the sky and the largest constellation in the zodiac. It lies between Leo to the west and Libra to the east.');
INSERT INTO public.constellation VALUES (3, 'Serpens Caput', 'The western part of the constellation, representing the serpent''s head, is located in the third quadrant of the northern hemisphere.');
INSERT INTO public.constellation VALUES (4, 'Ursa Major', 'Ursa Major is a constellation in the northern sky, whose associated mythology likely dates back into prehistory. Its Latin name means "greater bear," referring to and contrasting it with nearby Ursa Minor, the lesser bear');
INSERT INTO public.constellation VALUES (5, 'Canis Major', 'Canis Major is a constellation in the southern celestial hemisphere. In the second century, it was included in Ptolemy''s 48 constellations and is conunted among the 88 modern constellations. Its name is Latin for "greater dog" in contrast to the Canis Minor, the "lesser dog".');


--
-- Data for Name: galaxy; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy VALUES (1, 'Milky Way', NULL, 100000, NULL);
INSERT INTO public.galaxy VALUES (2, 'Andromeda', 'NGC 224', 152000, 2.54);
INSERT INTO public.galaxy VALUES (3, 'Tadpole', 'UGC 10214', 390000, 420.00);
INSERT INTO public.galaxy VALUES (4, 'Cigar', 'NGC 3034', 37000, 11.42);
INSERT INTO public.galaxy VALUES (5, 'Whirlpool', 'NGC 5194', 76000, 23.16);
INSERT INTO public.galaxy VALUES (6, 'Hoag''s Object', 'PGC 54559', 100000, 612.80);
INSERT INTO public.galaxy VALUES (7, 'Pinwheel', 'NGC 5457', 170000, 20.90);
INSERT INTO public.galaxy VALUES (8, 'Messier 49', 'NGC 4472', 160, 55.90);


--
-- Data for Name: galaxy_type; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.galaxy_type VALUES (1, 'Spiral', 'A galaxy exhibiting a central nucleus or barred structure from which extend curved arms of higher luminosity. They are also called spiral nebula.');
INSERT INTO public.galaxy_type VALUES (2, 'Elliptical', 'A galaxy that has a generally elliptical shape and that has no apparent internal structure or spiral arms.');
INSERT INTO public.galaxy_type VALUES (3, 'Ring', 'A galaxy having the shape of an elliptical ring, thought to be the result of a collision of two galaxies.');


--
-- Data for Name: moon; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.moon VALUES (1, 'Moon', 1737.4, 1609, 3);
INSERT INTO public.moon VALUES (2, 'Phobos', 11.1, 1877, 4);
INSERT INTO public.moon VALUES (3, 'Deimos', 6.2, 1877, 4);
INSERT INTO public.moon VALUES (4, 'Io', 1821.6, 1610, 5);
INSERT INTO public.moon VALUES (5, 'Europa', 1560.8, 1610, 5);
INSERT INTO public.moon VALUES (6, 'Callisto', 2410.0, 1610, 5);
INSERT INTO public.moon VALUES (7, 'Ganymede', 2631.0, 1610, 5);
INSERT INTO public.moon VALUES (8, 'Mimas', 198.6, 1789, 6);
INSERT INTO public.moon VALUES (9, 'Enceladus', 249.4, 1789, 6);
INSERT INTO public.moon VALUES (10, 'Tethys', 529.9, 1684, 6);
INSERT INTO public.moon VALUES (11, 'Dione', 560.0, 1684, 6);
INSERT INTO public.moon VALUES (12, 'Rhea', 764.0, 1672, 6);
INSERT INTO public.moon VALUES (13, 'Titan', 2575.0, 1655, 6);
INSERT INTO public.moon VALUES (14, 'Iapetus', 718.0, 1671, 6);
INSERT INTO public.moon VALUES (15, 'Miranda', 235.8, 1948, 7);
INSERT INTO public.moon VALUES (16, 'Ariel', 578.9, 1851, 7);
INSERT INTO public.moon VALUES (17, 'Umbriel', 584.7, 1851, 7);
INSERT INTO public.moon VALUES (18, 'Titania', 788.9, 1787, 7);
INSERT INTO public.moon VALUES (19, 'Oberon', 761.4, 1787, 7);
INSERT INTO public.moon VALUES (20, 'Triton', 1353.4, 1846, 8);
INSERT INTO public.moon VALUES (21, 'Nereid', 170.0, 1949, 8);


--
-- Data for Name: planet; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet VALUES (1, 'Mercury', 4879.4, 330220000, 0, false, true, 1);
INSERT INTO public.planet VALUES (2, 'Venus', 12104.0, 4868500000, 0, false, true, 1);
INSERT INTO public.planet VALUES (3, 'Earth', 12756.0, 5973600000, 1, true, true, 1);
INSERT INTO public.planet VALUES (4, 'Mars', 6779.0, 641850000, 2, false, true, 1);
INSERT INTO public.planet VALUES (5, 'Jupiter', 142800.0, 1898600000000, 79, false, true, 1);
INSERT INTO public.planet VALUES (6, 'Saturn', 120660.0, 568460000000, 82, false, true, 1);
INSERT INTO public.planet VALUES (7, 'Uranus', 51118.0, 86810000000, 27, false, true, 1);
INSERT INTO public.planet VALUES (8, 'Neptune', 49528.0, 102430000000, 14, false, true, 1);
INSERT INTO public.planet VALUES (9, 'Pluto', 2376.6, 13090000, 5, false, true, 1);
INSERT INTO public.planet VALUES (10, 'Eris', 2326.0, 16466000, 1, false, true, 1);
INSERT INTO public.planet VALUES (11, 'Haumea', 1560.0, 4006000, 2, false, false, 1);
INSERT INTO public.planet VALUES (12, 'Ceres', 939.0, 938350, 0, true, true, 1);


--
-- Data for Name: planet_type; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.planet_type VALUES (1, 'Terrestrial', 'Terrestrial planets are Earth-like planets made up of rocks or metals with a hard surface. They may also have a molten heavy-metal core and topological features such as valleys.');
INSERT INTO public.planet_type VALUES (2, 'Gass giant', 'A gas giant planet is a large planet mostly composed of helium and/or hydrogen. These planets don''t have hard surfaces and instead have swirling gases above a solid core.');
INSERT INTO public.planet_type VALUES (3, 'Ice giants', 'An ice giant is a giant planet composed mainly of elements heavier than hydrogen and helium, such as oxygen, carbon, nitrogen and sulphur.');
INSERT INTO public.planet_type VALUES (4, 'Dwarf', 'A dwarf planet is a small planetary-mass object that is in direct orbit of the Sun, smaller than any of the eight classical planets but still a world in its own right.');


--
-- Data for Name: star; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star VALUES (1, 'Sun', 0.0000158, 4.60, 5778, 1);
INSERT INTO public.star VALUES (2, 'Mizar', 82.6000000, 0.37, 9000, 7);
INSERT INTO public.star VALUES (3, 'Proxima Centauri', 4.2460000, 4.85, 3042, 1);
INSERT INTO public.star VALUES (4, 'Alioth', 82.6000000, 0.30, 9020, 8);
INSERT INTO public.star VALUES (5, 'Spica', 250.0000000, 12.50, 25300, 8);
INSERT INTO public.star VALUES (6, 'Sirius', 8.6100000, 0.24, 9940, 1);


--
-- Data for Name: star_type; Type: TABLE DATA; Schema: public; Owner: freecodecamp
--

INSERT INTO public.star_type VALUES (1, 'Yellow dwarf', 'A yellow dwarf is often referred to as a G-type main sequence star. A yellow dwarf has a mass almost like the mass of the Sun. It''s colour ranges from white to a lighter yellow.');
INSERT INTO public.star_type VALUES (2, 'White dwarf', 'A white dwarf is any of a class of faint stars representing the endpoint of the evolution of intermediate and low-mass stars. White dwarfs are so called because of the white colour of the first few that were discovered, are characterized by a low luminosity, a mass on the order of that of the Sun, and a radius comparable to that of the Earth.');
INSERT INTO public.star_type VALUES (3, 'Red dwarf', 'Red dwarf stars, also called M-type stars, are the most numerous type of star in the universe and the smallest type of hydrogen-burning star. Red dwarf stars have masses from about 0.08 to 0.6 times that of the Sun.');
INSERT INTO public.star_type VALUES (4, 'Blue giant', 'A blue giant is a hot star witha luminosity class of III or II. A bluish star that has a high surface temperature and a diameter that is large relative to the Sun.');
INSERT INTO public.star_type VALUES (5, 'Subgiant', 'A subgiant is a star that is brighter than a normal main-sequence star of the same spectral class, but not as bright as giant stars.');


--
-- Name: constellation_constellation_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.constellation_constellation_id_seq', 5, true);


--
-- Name: galaxy_galaxy_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_galaxy_id_seq', 8, true);


--
-- Name: galaxy_type_galaxy_type_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.galaxy_type_galaxy_type_id_seq', 3, true);


--
-- Name: moon_moon_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.moon_moon_id_seq', 22, true);


--
-- Name: planet_planet_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_planet_id_seq', 12, true);


--
-- Name: planet_type_planet_type_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.planet_type_planet_type_id_seq', 4, true);


--
-- Name: star_star_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_star_id_seq', 6, true);


--
-- Name: star_type_star_type_id_seq; Type: SEQUENCE SET; Schema: public; Owner: freecodecamp
--

SELECT pg_catalog.setval('public.star_type_star_type_id_seq', 5, true);


--
-- Name: constellation constellation_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.constellation
    ADD CONSTRAINT constellation_name_key UNIQUE (name);


--
-- Name: constellation constellation_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.constellation
    ADD CONSTRAINT constellation_pkey PRIMARY KEY (constellation_id);


--
-- Name: galaxy galaxy_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_name_key UNIQUE (name);


--
-- Name: galaxy galaxy_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy
    ADD CONSTRAINT galaxy_pkey PRIMARY KEY (galaxy_id);


--
-- Name: galaxy_type galaxy_type_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy_type
    ADD CONSTRAINT galaxy_type_name_key UNIQUE (name);


--
-- Name: galaxy_type galaxy_type_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.galaxy_type
    ADD CONSTRAINT galaxy_type_pkey PRIMARY KEY (galaxy_type_id);


--
-- Name: moon moon_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_name_key UNIQUE (name);


--
-- Name: moon moon_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_pkey PRIMARY KEY (moon_id);


--
-- Name: planet planet_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_name_key UNIQUE (name);


--
-- Name: planet planet_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_pkey PRIMARY KEY (planet_id);


--
-- Name: planet_type planet_type_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_type
    ADD CONSTRAINT planet_type_name_key UNIQUE (name);


--
-- Name: planet_type planet_type_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet_type
    ADD CONSTRAINT planet_type_pkey PRIMARY KEY (planet_type_id);


--
-- Name: star star_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_name_key UNIQUE (name);


--
-- Name: star star_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_pkey PRIMARY KEY (star_id);


--
-- Name: star_type star_type_name_key; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star_type
    ADD CONSTRAINT star_type_name_key UNIQUE (name);


--
-- Name: star_type star_type_pkey; Type: CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star_type
    ADD CONSTRAINT star_type_pkey PRIMARY KEY (star_type_id);


--
-- Name: moon moon_planet_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.moon
    ADD CONSTRAINT moon_planet_id_fkey FOREIGN KEY (planet_id) REFERENCES public.planet(planet_id);


--
-- Name: planet planet_star_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.planet
    ADD CONSTRAINT planet_star_id_fkey FOREIGN KEY (star_id) REFERENCES public.star(star_id);


--
-- Name: star star_galaxy_id_fkey; Type: FK CONSTRAINT; Schema: public; Owner: freecodecamp
--

ALTER TABLE ONLY public.star
    ADD CONSTRAINT star_galaxy_id_fkey FOREIGN KEY (galaxy_id) REFERENCES public.galaxy(galaxy_id);


--
-- PostgreSQL database dump complete
--

