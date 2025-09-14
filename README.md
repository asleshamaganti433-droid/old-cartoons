# old-cartoons
import { useState } from 'react';

function ClassicCartoonGallery() {
  const [selectedCartoon, setSelectedCartoon] = useState<number | null>(null);

  const handleCartoonClick = (index: number) => {
    setSelectedCartoon(selectedCartoon === index ? null : index);
  };

  return (
    <div className="min-h-screen bg-yellow-50 p-6">
      <div className="max-w-6xl mx-auto">
        <h1 className="text-4xl font-bold text-center mb-8 text-orange-600 font-serif">
          Vintage Toon Treasury
        </h1>
        <p className="text-center text-gray-700 mb-12 text-lg">
          A collection of classic animated characters from the golden age of animation
        </p>

        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
          {/* Mickey Mouse */}
          <div 
            className={`bg-white rounded-lg shadow-lg p-6 border-4 ${
              selectedCartoon === 0 ? 'border-red-500' : 'border-black'
            } transition-all duration-300 hover:scale-105 cursor-pointer`}
            onClick={() => handleCartoonClick(0)}
          >
            <div className="text-center mb-4">
              <h3 className="text-xl font-bold text-gray-800">Mickey Mouse</h3>
              <p className="text-sm text-gray-600">1928 - Walt Disney</p>
            </div>
            <div className="relative h-64 bg-gray-200 rounded-lg overflow-hidden">
              <img 
                src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/1566479f-2efb-4326-bbea-e1a6e98d3569.png" 
                alt="Classic black and white Mickey Mouse wearing his signature shorts and white gloves with a cheerful expression" 
                className="w-full h-full object-cover"
              />
            </div>
            {selectedCartoon === 0 && (
              <div className="mt-4 p-4 bg-yellow-100 rounded-lg border-2 border-dashed border-yellow-300">
                <p className="text-sm text-gray-700">
                  Mickey Mouse made his debut in "Steamboat Willie" and became the iconic character of The Walt Disney Company, known for his optimism and adventurous spirit.
                </p>
              </div>
            )}
          </div>

          {/* Bugs Bunny */}
          <div 
            className={`bg-white rounded-lg shadow-lg p-6 border-4 ${
              selectedCartoon === 1 ? 'border-red-500' : 'border-black'
            } transition-all duration-300 hover:scale-105 cursor-pointer`}
            onClick={() => handleCartoonClick(1)}
          >
            <div className="text-center mb-4">
              <h3 className="text-xl font-bold text-gray-800">Bugs Bunny</h3>
              <p className="text-sm text-gray-600">1940 - Warner Bros.</p>
            </div>
            <div className="relative h-64 bg-gray-200 rounded-lg overflow-hidden">
              <img 
                src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/0f12cae8-7dbc-4f72-9f47-29f062c64008.png" 
                alt="Bugs Bunny leaning on a carrot with a mischievous grin, wearing his typical relaxed pose and one eyebrow raised" 
                className="w-full h-full object-cover"
              />
            </div>
            {selectedCartoon === 1 && (
              <div className="mt-4 p-4 bg-yellow-100 rounded-lg border-2 border-dashed border-yellow-300">
                <p className="text-sm text-gray-700">
                  "What's up, Doc?" This clever rabbit from Looney Tunes is known for his Brooklyn accent, carrot-munching, and outsmarting his opponents with witty remarks.
                </p>
              </div>
            )}
          </div>

          {/* Popeye the Sailor */}
          <div 
            className={`bg-white rounded-lg shadow-lg p-6 border-4 ${
              selectedCartoon === 2 ? 'border-red-500' : 'border-black'
            } transition-all duration-300 hover:scale-105 cursor-pointer`}
            onClick={() => handleCartoonClick(2)}
          >
            <div className="text-center mb-4">
              <h3 className="text-xl font-bold text-gray-800">Popeye</h3>
              <p className="text-sm text-gray-600">1929 - King Features</p>
            </div>
            <div className="relative h-64 bg-gray-200 rounded-lg overflow-hidden">
              <img 
                src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/2def81cd-84bb-4df8-ab5a-50a4730ccace.png" 
                alt="Popeye the Sailor Man with bulging forearms, sailor hat, corncob pipe, and spinach can ready for action" 
                className="w-full h-full object-cover"
              />
            </div>
            {selectedCartoon === 2 && (
              <div className="mt-4 p-4 bg-yellow-100 rounded-lg border-2 border-dashed border-yellow-300">
                <p className="text-sm text-gray-700">
                  Popeye gains superhuman strength from eating spinach, helping him rescue his love Olive Oyl from the clutches of his rival Bluto.
                </p>
              </div>
            )}
          </div>

          {/* Betty Boop */}
          <div 
            className={`bg-white rounded-lg shadow-lg p-6 border-4 ${
              selectedCartoon === 3 ? 'border-red-500' : 'border-black'
            } transition-all duration-300 hover:scale-105 cursor-pointer`}
            onClick={() => handleCartoonClick(3)}
          >
            <div className="text-center mb-4">
              <h3 className="text-xl font-bold text-gray-800">Betty Boop</h3>
              <p className="text-sm text-gray-600">1930 - Fleischer Studios</p>
            </div>
            <div className="relative h-64 bg-gray-200 rounded-lg overflow-hidden">
              <img 
                src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/25eaa106-3083-430c-9c4e-cd4f3deba286.png" 
                alt="Betty Boop with her signature short black curly hair, large eyes, and flirtatious smile in her classic red dress" 
                className="w-full h-full object-cover"
              />
            </div>
            {selectedCartoon === 3 && (
              <div className="mt-4 p-4 bg-yellow-100 rounded-lg border-2 border-dashed border-yellow-300">
                <p className="text-sm text-gray-700">
                  One of the first animated sex symbols, Betty Boop was known for her jazz-age style, baby-talk voice, and innocent yet flirtatious personality.
                </p>
              </div>
            )}
          </div>

          {/* Tom and Jerry */}
          <div 
            className={`bg-white rounded-lg shadow-lg p-6 border-4 ${
              selectedCartoon === 4 ? 'border-red-500' : 'border-black'
            } transition-all duration-300 hover:scale-105 cursor-pointer`}
            onClick={() => handleCartoonClick(4)}
          >
            <div className="text-center mb-4">
              <h3 className="text-xl font-bold text-gray-800">Tom & Jerry</h3>
              <p className="text-sm text-gray-600">1940 - MGM</p>
            </div>
            <div className="relative h-64 bg-gray-200 rounded-lg overflow-hidden">
              <img 
                src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/77f67cef-be9f-4baa-be68-426e6f4c1c5d.png" 
                alt="Tom the cat chasing Jerry the mouse through a domestic setting with cartoonish action lines and exaggerated expressions" 
                className="w-full h-full object-cover"
              />
            </div>
            {selectedCartoon === 4 && (
              <div className="mt-4 p-4 bg-yellow-100 rounded-lg border-2 border-dashed border-yellow-300">
                <p className="text-sm text-gray-700">
                  The classic cat-and-mouse duo known for their slapstick comedy, elaborate chase sequences, and occasional moments of friendship amidst their rivalry.
                </p>
              </div>
            )}
          </div>

          {/* Woody Woodpecker */}
          <div 
            className={`bg-white rounded-lg shadow-lg p-6 border-4 ${
              selectedCartoon === 5 ? 'border-red-500' : 'border-black'
            } transition-all duration-300 hover:scale-105 cursor-pointer`}
            onClick={() => handleCartoonClick(5)}
          >
            <div className="text-center mb-4">
              <h3 className="text-xl font-bold text-gray-800">Woody Woodpecker</h3>
              <p className="text-sm text-gray-600">1940 - Walter Lantz</p>
            </div>
            <div className="relative h-64 bg-gray-200 rounded-lg overflow-hidden">
              <img 
                src="https://storage.googleapis.com/workspace-0f70711f-8b4e-4d94-86f1-2a93ccde5887/image/3d6a3c5a-e3cd-4869-a525-044ae356b34f.png" 
                alt="Woody Woodpecker with his distinctive red crest, blue feathers, and mischievous laughing expression with one eye closed" 
                className="w-full h-full object-cover"
              />
            </div>
            {selectedCartoon === 5 && (
              <div className="mt-4 p-4 bg-yellow-100 rounded-lg border-2 border-dashed border-yellow-300">
                <p className="text-sm text-gray-700">
                  Known for his iconic laugh and mischievous personality, Woody Woodpecker was created by Walter Lantz and became one of animation's most recognizable characters.
                </p>
              </div>
            )}
          </div>
        </div>
      </div>
    </div>
  );
}

export default ClassicCartoonGallery;
